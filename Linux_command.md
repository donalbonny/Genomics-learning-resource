# List of helpful Linux commands to process FASTQ, FASTA files from NGS experiments
A file storing biological sequences with extension ‘.fastq’ is a file in FASTQ format, if it is also compressed with GZIP  the suffix will be ‘.fastq.gz’ 

##### 1.  Compress a FASTQ file in GZIP format:

```gzip reads.fastq```

##### 2. Check the contents of the file we can use the command ‘less’ or ‘zless’:

``` less reads.fastq.gz```
``` zless reads.fastq.gz```
 

##### 3.  If the file is in FASTA format, we will count the number of sequences like this:

 ```grep -c "^>" reads.fa```
 
 ##### 4. Count the number of reads in FASTQ files
 ```echo $(cat yourfile.fastq|wc -l)/4|bc  ```
 
 ##### 5. count how many times appear an specific subsequence:

``` zgrep -c 'ATGATGATG' reads.fq.gz ```

##### 6. How much disk space is using the compressed file:
```zcat reads.fq.gz | wc --bytes```

#### Reference:
1. http://darrenjw.wordpress.com/2010/11/28/introduction-to-the-processing-of-short-read-next-generation-sequencing-data/





