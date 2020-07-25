I collected these tips from [Bioinformatics Dat Skills  Book](https://vincebuffalo.com/book/) while reading the book:

### Organizing Data to Automate File Processing Tasks

1. Create the zmays-snps/project directories:

$ mkdir -p zmays-snps/{data/seqs,scripts,analysis}

this creates the three subdirectories (and saves you having to type “zmayssnps/” three times). -p is used to tell mkdir to create any necessary subdirectories it needs 


2. Common Unix filename wildcards

* Zero or more characters ( but ignore hidden files tarting with a period)
? One character
[A-Z] Any character between the supplied alphanumerica range

