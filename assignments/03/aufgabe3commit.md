# 1.How to get the first three lines of the file 2014-01_JA.tsv:
$ head -n 3 /c/Users/tareh/OneDrive/shell-lesson/2014-01_JA.tsv
<br>
Output: <br>
File    Creator Issue   Volume  Journal ISSN    ID      Citation        Title  Place Labe       Language        Publisher       Date
History_1a-rdf.tsv      Doolittle, W. E.        1       59      KIVA -ARIZONA- 0023-1940        (Uk)RN001571862 KIVA -ARIZONA- 59(1), 7-26. (1993)      A Method for Distinguishing between Prehistoric and Recent Water and Soil Control Features      xxu     eng     ARIZONA ARCHAEOLOGICAL AND HISTORICAL SOCIETY   1993
History_1a-rdf.tsv      Nelson, M. C.   1       59      KIVA -ARIZONA-  0023-1940       (Uk)RN001571874 KIVA -ARIZONA- 59(1), 27-48. (1993)     Classic Mimbres Land Use in the Eastern Mimbres Region, Southwestern New Mexico xxu     eng    ARIZONA ARCHAEOLOGICAL AND HISTORICAL SOCIETY    1993

# 2.How to get the total number of lines in each of the *.tsv files:
$ wc -l *.tsv
<br><br>
Output: <br>
    13712 2014-01-31_JA-africa.tsv
    27392 2014-01-31_JA-america.tsv
   507732 2014-01_JA.tsv
     5375 2014-02-02_JA-britain.tsv
   554211 total

# 3.How do you get the file with the highest number of lines and how many does it have? Canyou geth the Output with a single command line call?
$ wc -l *.tsv | grep -v ' total' | sort -n | tail -1
<br><br>
Output: <br>
   507732 2014-01_JA.tsv
