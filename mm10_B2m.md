primer design for beta 2 microglobulin for mouse mm10 reference

1. Navigate to B2m gene for mm10 genome on ucsc genome browser

2. Click on the gene to retrieve the ensembl transcript number and refseq accession
```
Description: Mus musculus beta-2 microglobulin (B2m), mRNA. (from RefSeq NM_009735)
Gencode Transcript: ENSMUST00000102476.4
Gencode Gene: ENSMUSG00000060802.8

RefSeq Accession: NM_009735.3
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


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000102476.4) because other genes that overlap the same region will also have sequences. 
```
>mm10_knownGene_ENSMUST00000102476.4 range=chr2:122147738-122151660 5'pad=0 3'pad=0 strand=+ repeatMasking=N
ATGGCTCGCTCGGTGACCCTGGTCTTTCTGGTGCTTGTCTCACTGACCGG
CCTGTATGCTATCCAGAAAACCCCTCAAATTCAAGTATACTCACGCCACC
CACCGGAGAATGGGAAGCCGAACATACTGAACTGCTACGTAACACAGTTC
CACCCGCCTCACATTGAAATCCAAATGCTGAAGAACGGGAAAAAAATTCC
TAAAGTAGAGATGTCAGATATGTCCTTCAGCAAGGACTGGTCTTTCTATA
TCCTGGCTCACACTGAATTCACCCCCACTGAGACTGATACATACGCCTGC
AGAGTTAAGCATGCCAGTATGGCCGAGCCCAAGACCGTCTACTGGGATCG
AGACATGTGA

```

4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY   SCORE START   END QSIZE IDENTITY  CHROM              STRAND  START       END   SPAN
------------------------------------------------------------------------------------------------------------------------
browser new tab details YourSeq   345     1   346   360   100.0%  chr2               +   122147738 122151151   3414
browser new tab details YourSeq    33    29    78   360    97.2%  chr5               +    32529231  32906842 377612
browser new tab details YourSeq    21   207   227   360   100.0%  chr12              -    55888778  55888798     21
browser new tab details YourSeq    20   221   240   360   100.0%  chr4_JH584326_alt  -     1588034   1588053     20   What is chrom_alt?
browser new tab details YourSeq    20   221   240   360   100.0%  chr4               -   151282613 151282632     20
browser new tab details YourSeq    20   239   258   360   100.0%  chr4               -    82720851  82720870     20
browser new tab details YourSeq    20   189   210   360    95.5%  chr6               +    28093886  28093907     22
```
Note how there is a 100% match for the region of interest and a partial match for regions on other chromosomes


4. Navigate to NCBI primer blast
Paste the refseq accession NM_009735.3 into the PCR template box
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
Forward primer	TCACACTGAATTCACCCCCA	Plus	20	309	328	58.86	50.00	8.00	0.00
Reverse primer	TCACATGTCTCGATCCCAGT	Minus	20	411	392	58.15	50.00	6.00	2.00
Product length	103
Exon junction	397/398 (reverse primer) on template NM_009735.3
Products on intended targets
>NM_009735.3 Mus musculus beta-2 microglobulin (B2m), mRNA

product length = 103
Forward primer  1    TCACACTGAATTCACCCCCA  20
Template        309  ....................  328

Reverse primer  1    TCACATGTCTCGATCCCAGT  20
Template        411  ....................  392
```

Make sure the primer pair has no off target effects

5. Double check primers with gene sequence on NBCI primer blast



