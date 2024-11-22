# Data Analysis of LOTR Dialogs

This document provides an analysis of the LOTR dialogs dataset. The analysis was conducted to answer specific questions about the dataset.

---

## 1. Total Lines and Unique Words
- *Total number of lines in the dialogs*: 2,390
- *Total number of unique words in the dialogs*: 6,200

---

## 2. Distribution of Dialogs Across the Films
| Film                          | Number of Lines |
|-------------------------------|-----------------|
| The Two Towers                | 1,010           |
| The Return of the King        | 873             |
| The Fellowship of the Ring    | 507             |

---

## 3. Top 5 Characters in the char Column
| Character  | Occurrences |
|------------|-------------|
| FRODO      | 225         |
| SAM        | 216         |
| GANDALF    | 204         |
| ARAGORN    | 185         |
| PIPPIN     | 163         |

---

## 4. Top 5 Characters in the Dialogs (Total Words Spoken)
| Character  | Total Words |
|------------|-------------|
| GANDALF    | 3,169       |
| SAM        | 2,079       |
| FRODO      | 1,749       |
| ARAGORN    | 1,429       |
| GOLLUM     | 1,317       |

---

## Shell Commands for Reproducibility

Below are the shell commands you can use to replicate this analysis.

1. *Total number of lines and unique words in the dialogs*:
   bash
   # Count total lines
   wc -l lotr_scripts.csv

   # Count unique words in the dialogs
   cut -d',' -f3 lotr_scripts.csv | tr ' ' '\n' | sort | uniq | wc -l
   

2. *Distribution of dialogs across the three films*:
   bash
   # Count the number of lines per film
   cut -d',' -f4 lotr_scripts.csv | sort | uniq -c
   

3. **Top 5 characters in the char column**:
   bash
   # Count occurrences of each character
   cut -d',' -f2 lotr_scripts.csv | sort | uniq -c | sort -nr | head -5


4. *Top 5 characters by total words spoken*:
   bash
   # Count total words spoken by each character
   awk -F',' '{print $2, gsub(" ", " ", $3)}' lotr_scripts.csv | awk '{a[$1]+=$2} END {for (i in a) print a[i], i}' | sort -nr | head -5

   
