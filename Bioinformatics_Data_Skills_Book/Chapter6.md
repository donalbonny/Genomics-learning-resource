### Chapter 6: Bioinformatics Data

1. Downloading data with  wget, curl, Rsync and Secure Copy (scp)

2. Rsync and Secure Copy (scp)
wget and curl are appropriate for quickly downloading files from the command line, but are not optimal for some heavier-duty tasks

```rsync -avz -e ssh zea_mays/data/ vinceb@[...]:/home/deborah/zea_mays/data```

-azv: The option -a enables wrsync’s archive mode, -z enables file transfer compression, and -v makes rsync’s progress more verbose so you can see what’s being transferred

scp example: ```scp Zea_mays.AGPv3.20.gtf 192.168.237.42:/home/deborah/zea_mays/data/```

3. Data Integrity 

To verify transferred data's intergrity with checksum. Checksums are very compressed summaries of data, computed in a way that even if just one bit of the data is changed, the checksum will be different

The two most common checksum algorithms for ensuring data integrity are MD5 and SHA-1

On Linux:

To obtain checksum using SHA-1 and md5 

```shasum filename ```

```md5sum file name ```

To obtain MD5 sum for a list of files in a folder: 

```find -type f -exec md5sum {} \; > md5.list```

``` shasum data/*.fastq > fastq_chechsum.sha```

For Window Powershell

```Get-FileHash <filepath> -Algorithm MD5```

```CertUtil -hashfile <file path>   MD5```






