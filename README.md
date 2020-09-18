# One-Liners
A short of useful one liners to move around easily.

Here I describe a set of one liners, that I come across and I think are extremely useful

Convert to fasta from fastq

```
sed -n '1~4s/^@/>/p;2~4p' <REV>_JOINED.fastq > <REV>_JOINED.fasta
```

Add the total sum of one column

```
awk '{ total += $2; count++ } END { print total/count }'
```

Get the average of one column

```
awk '{sum+=$1; sumsq+=$1*$1} END {print sqrt(sumsq/NR - (sum/NR)**2)}'
```

Add the total sum of one column by index located on another column

```
awk '{a[$1]+=$2}END{for(i in a) print i,a[i]}'
```

Count the number of columns in a file

```
awk -F '|' '{print NF; exit}' <file name>
```

Extract a subset of lines from a large file 

```
sed -n 11551,13475p results6801.csv  
```
