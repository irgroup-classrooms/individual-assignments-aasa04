0.Create project <br>
1.Rename column Column to Index <br>
2.Mass edit 1 cells in column char <br>
3.Mass edit 1 cells in column dialog <br>
4.Text transform on 2.320 cells in column dialog: value.trim() <br>
5.Text transform on 568 cells in column dialog: grel:value.replace(/\s+/ , " ") <br>
6.Text transform on 10 cells in column dialog: grel:value.replace(/^\s*,/, "") <br>
7.Text transform on 8 cells in column dialog: grel:value.trim() <br>
8.Text transform on 333 cells in column dialog: grel:value.replace(/\s+,/, ",").replace(/,\s+/, ", ") <br>
9.Text transform on 13 cells in column dialog: grel:value.replace(/,{2,}/, ",") <br>
10.Text transform on 16 cells in column dialog: grel:value.replace(")", "") <br>
11.Text transform on 86 cells in column dialog: grel:value.replace(/!,+/, "!") <br>
12.Text transform on 195 cells in column dialog: grel:value.replace(/\.\s*,/, ".") <br>
13.Text transform on 209 cells in column dialog: grel:value.replace(/([^.!?])$/, "$1.") <br>
14.Text transform on 2.390 cells in column Index: grel:rowIndex + 1 
