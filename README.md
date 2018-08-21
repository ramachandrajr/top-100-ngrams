# command used to extract from fusion tables
cut -d',' -f1 ngrams2.csv | head -n 100 > top100_2letter_sequences.txt

# convert full file from upper case to lower case 
tr '[:upper:]' '[:lower:]' < ngrams3.txt > ngrams3_1.txt;mv ngrams3_1.txt ngrams3.txt

sed -e ':a' -e 'N' -e '$!ba' -e 's/\n/ /g' ngrams4.txt > ngrams4-1.txt; mv ngrams4-1.txt ngrams4.txt; tr '[:upper:]' '[:lower:]' < ngrams4.txt > ngrams4_1.txt; mv ngrams4_1.txt ngrams4.txt
