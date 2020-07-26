# Sequences and Genomic Features

### Genome annotation

[BED format](http://genome.ucsc.edu/FAQ/FAQformat.html#format1): BED (Browser Extensible Data) format provides a flexible way to define the data lines that are displayed in an annotation track. BED lines have three required fields and nine additional optional fields. 

[GTF/GFF (General Transfer Format/General Feature Format) ](http://genome.ucsc.edu/FAQ/FAQformat.html#format4) 

GTF2.2 is an extension to, and backward compatible with, GFF2. The first eight GTF fields are the same as GFF. The feature field is the same as GFF, with the exception that it also includes the following optional values: 5UTR, 3UTR, inter, inter_CNS, and intron_CNS. The group field has been expanded into a list of attributes. Each attribute consists of a type/value pair. Attributes must end in a semi-colon, and be separated from any following attribute by exactly one space.

The attribute list must begin with the two mandatory attributes:

- gene_id value - A globally unique identifier for the genomic source of the sequence.
- transcript_id value - A globally unique identifier for the predicted transcript.

[Data file format resource from UCSC](http://genome.ucsc.edu/FAQ/FAQformat.html#format3)

### Samtools

samtools 
-- Indexing
     dict           create a sequence dictionary file
     faidx          index/extract FASTA
     fqidx          index/extract FASTQ
     index          index alignment

  -- Editing
     calmd          recalculate MD/NM tags and '=' bases
     fixmate        fix mate information
     reheader       replace BAM header
     targetcut      cut fosmid regions (for fosmid pool only)
     addreplacerg   adds or replaces RG tags
     markdup        mark duplicates

  -- File operations
     collate        shuffle and group alignments by name
     cat            concatenate BAMs
     merge          merge sorted alignments
     mpileup        multi-way pileup
     sort           sort alignment file
     split          splits a file by read group
     quickcheck     quickly check if SAM/BAM/CRAM file appears intact
     fastq          converts a BAM to a FASTQ
     fasta          converts a BAM to a FASTA

  -- Statistics
     bedcov         read depth per BED region
     coverage       alignment depth and percent coverage
     depth          compute the depth
     flagstat       simple stats
     idxstats       BAM index stats
     phase          phase heterozygotes
     stats          generate stats (former bamcheck)

  -- Viewing
     flags          explain BAM flags
     tview          text alignment viewer
     view           SAM<->BAM<->CRAM conversion
     depad          convert padded BAM to unpadded BAM
     
 1. How many alignments does bam file contain?  
     ```samtools flagstat sample.bam```
     
2. Sort file for indexing, for visualization 

```nohup samtools sort input.bam input.sorted.bam &```

This is quite extensive 
'nohup' (no hangup) that's to prevent any interruption from the curretn terminal to be transmitted. 

Note: nohup is a POSIX command to ignore the HUP (hangup) signal. The HUP signal is, by convention, the way a terminal warns dependent processes of logout.
Output that would normally go to the terminal goes to a file called nohup.out if it has not already been redirected.

'2>&1' - redirect stderr to stdout

The trailing '&' operator at the end of a command is used to put commands into background. 

3. Generate index file for bam file > generate .bam.bai 

```samtools index example.sorted.bam```

4. How to merge bam files?

``` nohup samtools merge sample.bam sample1.bam sample2.bam &```

5. samtools view: 

```samtools view sample1.bam | more ```  convert to sam form with no header information 
     
```samtools view -h sample1.bam | more```  contain with header information
     
```samtools view -H sample1.bam ```  print only header 

```samtools view -bT /reference_file/hg38.fa example.sam > sample.sam.bam``` convert sam to bam 
     
```samtools view example.bam  "chr2:24000-25000000"```  view regions, only apply for indexed BAM or CRAM files

```samtools view -L  example.bed example.bam  | head``` specify the regions in bed file 


### Bedtools 




     
     
     



