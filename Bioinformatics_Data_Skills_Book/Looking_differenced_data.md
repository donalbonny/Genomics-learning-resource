### Looking at Differences Between Data

One approach to this is to compute the diff between two files using the Unix tool diff. Unix’s diff works line by line, and outputs blocks (called hunks) that differ between files

```diff -u gene-1.bed gene-2.bed```
