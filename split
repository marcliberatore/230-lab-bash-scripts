#!/bin/bash

dirname=lines
extension=.txt
rm -r $dirname
mkdir $dirname
sourcefile=aladdin.txt
counter=0

while IFS= read -r line; do
  filename=$dirname\/$(printf $counter)$extension
  echo "$line" > $filename
  ((counter++))
done < $sourcefile
  
