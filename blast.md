Already got database for genome assembly. 

Run BLASTN of our sequence against the genome assembly to check if we've amplified the right locus.

```
#!/bin/sh
#PBS -l walltime=1:00:00
#PBS -l cput=1:00:00
#PBS -l nodes=1:centos6
#PBS -d /export/home2/jmi45g/Tc22_1mc/blast

export PATH="/export/home/jmi45g/anaconda3/envs/BLAST_tools/bin:$PATH"

blastn -query S1.fa -db TcCANU2.2+SALSA_030822 -out S1_TcCANU2.2+SALSA_030822.blastn6 -evalue 1e-05 -outfmt 6
```


```
#!/bin/sh
#PBS -l walltime=1:00:00
#PBS -l cput=1:00:00
#PBS -l nodes=1:centos6
#PBS -d /export/home2/jmi45g/Tc22_1mc/blast

export PATH="/export/home/jmi45g/anaconda3/envs/BLAST_tools/bin:$PATH"

blastn -query S8.fa -db TcCANU2.2+SALSA_030822 -out S8_TcCANU2.2+SALSA_030822.blastn6 -evalue 1e-05 -outfmt 6
```

