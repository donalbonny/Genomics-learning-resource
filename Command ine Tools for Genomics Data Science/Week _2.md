# Sequences and Genomic Features

### Genome annotation

[BED format](http://genome.ucsc.edu/FAQ/FAQformat.html#format1): BED (Browser Extensible Data) format provides a flexible way to define the data lines that are displayed in an annotation track. BED lines have three required fields and nine additional optional fields. 

[GTF/GFF (General Transfer Format/General Feature Format) ](http://genome.ucsc.edu/FAQ/FAQformat.html#format4) 

GTF2.2 is an extension to, and backward compatible with, GFF2. The first eight GTF fields are the same as GFF. The feature field is the same as GFF, with the exception that it also includes the following optional values: 5UTR, 3UTR, inter, inter_CNS, and intron_CNS. The group field has been expanded into a list of attributes. Each attribute consists of a type/value pair. Attributes must end in a semi-colon, and be separated from any following attribute by exactly one space.

The attribute list must begin with the two mandatory attributes:

- gene_id value - A globally unique identifier for the genomic source of the sequence.
- transcript_id value - A globally unique identifier for the predicted transcript.

[Data file format resource from UCSC] (http://genome.ucsc.edu/FAQ/FAQformat.html#format3)


