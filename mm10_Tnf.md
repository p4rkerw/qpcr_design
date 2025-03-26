primer design for Tnf for mouse mm10 reference

1. Navigate to gene for mm10 genome on ucsc genome browser

2. Click on the gene to retrieve the ensembl transcript number and refseq accession
```
Description: Mus musculus tumor necrosis factor (Tnf), transcript variant 1, mRNA. (from RefSeq NM_013693)
Gencode Transcript: ENSMUST00000025263.14
Gencode Gene: ENSMUSG00000024401.14

RefSeq Accession: NM_013693.3
```

3. Retrieve the DNA sequence of the gene using the Table Browser tool
Tools > Table Browser

```
Clade: Mammal  Genome: Mouse  Assembly: Dec. 2011 GRCm38/mm10
Group: Genes and Gene Predictions  Track: GENCODE VM23
Table: knownGene

Output Format: Sequence
```
Select sequence type for GENCODE VM23 > genomic

Sequence retrieval options: 
CDS Exons
One FASTA record per gene

Sequnece Formatting Options:
Mask repeats to N


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000025263.14) because other genes that overlap the same region will also have sequences. 
```
>mm10_knownGene_ENSMUST00000025263.14 range=chr17:35200145-35201840 5'pad=0 3'pad=0 strand=- repeatMasking=N
ATGAGCACAGAAAGCATGATCCGCGACGTGGAACTGGCAGAAGAGGCACT
CCCCCAAAAGATGGGGGGCTTCCAGAACTCCAGGCGGTGCCTATGTCTCA
GCCTCTTCTCATTCCTGCTTGTGGCAGGGGCCACCACGCTCTTCTGTCTA
CTGAACTTCGGGGTGATCGGTCCCCAAAGGGATGAGAAGTTCCCAAATGG
CCTCCCTCTCATCAGTTCTATGGCCCAGACCCTCACACTCAGATCATCTT
CTCAAAATTCGAGTGACAAGCCTGTAGCCCACGTCGTAGCAAACCACCAA
GTGGAGGAGCAGCTGGAGTGGCTGAGCCAGCGCGCCAACGCCCTCCTGGC
CAACGGCATGGATCTCAAAGACAACCAACTAGTGGTGCCAGCCGATGGGT
TGTACCTTGTCTACTCCCAGGTTCTCTTCAAGGGACAAGGCTGCCCCGAC
TACGTGCTCCTCACCCACACCGTCAGCCGATTTGCTATCTCATACCAGGA
GAAAGTCAACCTCCTCTCTGCCGTCAAGAGCCCCTGCCCCAAGGACACCC
CTGAGGGGGCTGAGCTCAAACCCTGGTATGAGCCCATATACCTGGGAGGA
GTCTTCCAGCTGGAGAAGGGGGACCAACTCAGCGCTGAGGTCAATCTGCC
CAAGTACTTAGACTTTGCGGAGTCCGGGCAGGTCTACTTTGGAGTCATTG
CTCTGTGA

```

4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY   SCORE START   END QSIZE IDENTITY  CHROM               STRAND  START       END   SPAN
-------------------------------------------------------------------------------------------------------------------------
browser new tab details YourSeq   705     1   708   708   100.0%  chr17_JH584328_alt  -     1518315   1520010   1696   What is chrom_alt?
browser new tab details YourSeq   705     1   708   708   100.0%  chr17_JH584266_alt  -     1518552   1520247   1696   What is chrom_alt?
browser new tab details YourSeq   705     1   708   708   100.0%  chr17_GL456022_alt  -     1449830   1451525   1696   What is chrom_alt?
browser new tab details YourSeq   705     1   708   708   100.0%  chr17               -    35200145  35201840   1696
browser new tab details YourSeq    28   527   561   708    91.0%  chr10               +    31449543  31449581     39
browser new tab details YourSeq    27   533   568   708    96.6%  chr3                -   109094947 109094983     37
browser new tab details YourSeq    25   299   327   708    96.3%  chr1                +   190106087 190106119     33
browser new tab details YourSeq    21   115   136   708   100.0%  chr11               -    63149959  63149981     23
browser new tab details YourSeq    21   685   705   708   100.0%  chr10               +    78920873  78920893     21
browser new tab details YourSeq    21   685   705   708   100.0%  chr10               +    78959229  78959249     21
browser new tab details YourSeq    20    97   116   708   100.0%  chr15               -   102735243 102735262     20
browser new tab details YourSeq    20   291   310   708   100.0%  chr11               -    96539754  96539773     20
```
Note how there is a 100% match for the region of interest and a partial match for regions on other chromosomes


4. Navigate to NCBI primer blast
Paste the refseq accession NM_013693.3 into the PCR template box
Decrease the PCR product maximum size from 1000 to 150

Exon/intron selection
> Exon junction span: Primer must span an exon-exon junction

Primer pair specificity checking parameters
Database: Refseq mRNA
Organism: Mus musculus (taxid:10090)

Get Primers

```
Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	TAGCCCACGTCGTAGCAAAC	Plus	20	442	461	60.39	55.00	5.00	0.00
Reverse primer	ACAAGGTACAACCCATCGGC	Minus	20	577	558	60.32	55.00	4.00	2.00
Product length	136
Exon junction	456/457 (forward primer) on template NM_013693.3
Products on intended targets
>NM_013693.3 Mus musculus tumor necrosis factor (Tnf), transcript variant 1, mRNA

product length = 136
Forward primer  1    TAGCCCACGTCGTAGCAAAC  20
Template        442  ....................  461

Reverse primer  1    ACAAGGTACAACCCATCGGC  20
Template        577  ....................  558


```

Make sure the primer pair has no off target effects

5. Double check primers with refseq accession and/or sequence on NBCI primer blast
```
Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	TAGCCCACGTCGTAGCAAAC	Plus	20	275	294	60.39	55.00	5.00	0.00
Reverse primer	ACAAGGTACAACCCATCGGC	Minus	20	410	391	60.32	55.00	4.00	2.00
Product length	136
```


