0.Create project
1.Rename column Column to Index
2.Mass edit 1 cells in column char
3.Mass edit 1 cells in column dialog
4.Text transform on 2.320 cells in column dialog: value.trim()
5.Text transform on 568 cells in column dialog: grel:value.replace(/\s+/ , " ")
6.Text transform on 10 cells in column dialog: grel:value.replace(/^\s*,/, "")
7.Text transform on 8 cells in column dialog: grel:value.trim()
8.Text transform on 333 cells in column dialog: grel:value.replace(/\s+,/, ",").replace(/,\s+/, ", ")
9.Text transform on 13 cells in column dialog: grel:value.replace(/,{2,}/, ",")
10.Text transform on 16 cells in column dialog: grel:value.replace(")", "")
11.Text transform on 86 cells in column dialog: grel:value.replace(/!,+/, "!")
12.Text transform on 195 cells in column dialog: grel:value.replace(/\.\s*,/, ".")
13.Text transform on 209 cells in column dialog: grel:value.replace(/([^.!?])$/, "$1.")
14.Text transform on 2.390 cells in column Index: grel:rowIndex + 1
