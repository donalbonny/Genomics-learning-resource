#List of helpful Linux commands to process FASTQ, FASTA files from NGS experiments
A file storing biological sequences with extension ‘.fastq’ is a file in FASTQ format, if it is also compressed with GZIP  the suffix will be ‘.fastq.gz’ 
1.  compress a FASTQ file in GZIP format:

```
gzip reads.fastq
```

2. check the contents of the file we can use the command ‘less’ or ‘zless’:

```
 less reads.fastq.gz
 zless reads.fastq.gz
```

