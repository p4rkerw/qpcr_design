primer design for Tnfrsf1a for mouse mm10 reference

1. Navigate to gene for mm10 genome on ucsc genome browser

2. Click on the gene to retrieve the ensembl transcript number and refseq accession
```
Description: Mus musculus tumor necrosis factor receptor superfamily, member 1a (Tnfrsf1a), mRNA. (from RefSeq NM_011609)
Gencode Transcript: ENSMUST00000032491.14
Gencode Gene: ENSMUSG00000030341.17

RefSeq Accession: NM_011609.4
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


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000032491.14) because other genes that overlap the same region will also have sequences. 
```
>mm10_knownGene_ENSMUST00000032491.14 range=chr6:125350024-125361994 5'pad=0 3'pad=0 strand=+ repeatMasking=N
ATGGGTCTCCCCACCGTGCCTGGCCTGCTGCTGTCACTGGTGCTCCTGGC
TCTGCTGATGGGGATACATCCATCAGGGGTCACTGGACTAGTCCCTTCTC
TTGGTGACCGGGAGAAGAGGGATAGCTTGTGTCCCCAAGGAAAGTATGTC
CATTCTAAGAACAATTCCATCTGCTGCACCAAGTGCCACAAAGGAACCTA
CTTGGTGAGTGACTGTCCGAGCCCAGGGCGGGATACAGTCTGCAGGGAGT
GTGAAAAGGGCACCTTTACGGCTTCCCAGAATTACCTCAGGCAGTGTCTC
AGTTGCAAGACATGTCGGAAAGAAATGTCCCAGGTGGAGATCTCTCCTTG
CCAAGCTGACAAGGACACGGTGTGTGGCTGTAAGGAGAACCAGTTCCAAC
GCTACCTGAGTGAGACACACTTCCAGTGCGTGGACTGCAGCCCCTGCTTC
AACGGCACCGTGACAATCCCCTGTAAGGAGACTCAGAACACCGTGTGTAA
CTGCCATGCAGGGTTCTTTCTGAGAGAAAGTGAGTGCGTCCCTTGCAGCC
ACTGCAAGAAAAATGAGGAGTGTATGAAGTTGTGCCTACCTCCTCCGCTT
GCAAATGTCACAAACCCCCAGGACTCAGGTACTGCGGTGCTGTTGCCCCT
GGTTATCTTGCTAGGTCTTTGCCTTCTATCCTTTATCTTCATCAGTTTAA
TGTGCCGATATCCCCGGTGGAGGCCCGAAGTCTACTCCATCATTTGTAGG
GATCCCGTGCCTGTCAAAGAGGAGAAGGCTGGAAAGCNNNNNNNNNNNNN
NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
NNNNNNNNCCAGGCTTTAGTTCTCCTGTCTCCAGTACCCCCATCAGCCCC
ATCTTCGGTCCTAGTAACTGGCACTTCATGCCACCTGTCAGTGAGGTAGT
CCCAACCCAGGGAGCTGACCCTCTGCTCTACGAATCACTCTGCTCCGTGC
CAGCCCCCACCTCTGTTCAGAAATGGGAAGACTCCGCCCACCCGCAACGT
CCTGACAATGCAGACCTTGCGATTCTGTATGCTGTGGTGGATGGCGTGCC
TCCAGCGCGCTGGAAGGAGTTCATGCGTTTCATGGGGCTGAGCGAGCACG
AGATCGAGAGGCTGGAGATGCAGAACGGGCGCTGCCTGCGCGAGGCTCAG
TACAGCATGCTGGAAGCCTGGCGGCGCCGCACGCCGCGCCACGAGGACAC
GCTGGAAGTAGTGGGCCTCGTGCTTTCCAAGATGAACCTGGCTGGGTGCC
TGGAGAATATCCTCGAGGCTCTGAGAAATCCCGCCCCCTCGTCCACGACC
CGCCTCCCGCGATAA

```

4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY                                SCORE START   END QSIZE IDENTITY  CHROM  STRAND  START       END   SPAN
-----------------------------------------------------------------------------------------------------------------------------------------
browser new tab details mm10_knownGene_ENSMUST00000032491.14  1285     1  1365  1365   100.0%  chr6   +   125350024 125361994  11971
browser new tab details mm10_knownGene_ENSMUST00000032491.14    29   603   700  1365    58.1%  chr13  -    81793190  81793236     47
browser new tab details mm10_knownGene_ENSMUST00000032491.14    23   763   786  1365   100.0%  chr10  +    44895876  44895901     26
browser new tab details mm10_knownGene_ENSMUST00000032491.14    22   738   759  1365   100.0%  chr6   +    46853685  46853706     22
browser new tab details mm10_knownGene_ENSMUST00000032491.14    22   160   184  1365    96.0%  chr10  +    84333511  84333537     27
browser new tab details mm10_knownGene_ENSMUST00000032491.14    20   151   170  1365   100.0%  chr12  -    57406125  57406144     20
browser new tab details mm10_knownGene_ENSMUST00000032491.14    20  1013  1032  1365   100.0%  chr11  -    89694898  89694917     20
browser new tab details mm10_knownGene_ENSMUST00000032491.14    20    25    44  1365   100.0%  chr14  +    29438406  29438425     20
browser new tab details mm10_knownGene_ENSMUST00000032491.14    20   151   170  1365   100.0%  chr10  +   111851753 111851772     20
```
Note how there is a 100% match for the region of interest and a partial match for regions on other chromosomes


4. Navigate to NCBI primer blast
Paste the refseq accession NM_011609.4 into the PCR template box
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
Forward primer	AGTGAGGTAGTCCCAACCCA	Plus	20	1241	1260	59.81	55.00	3.00	3.00
Reverse primer	TCGCAAGGTCTGCATTGTCA	Minus	20	1373	1354	60.25	50.00	4.00	3.00
Product length	133
Exon junction	1358/1359 (reverse primer) on template NM_011609.4
Products on intended targets
>NM_011609.4 Mus musculus tumor necrosis factor receptor superfamily, member 1a (Tnfrsf1a), mRNA

product length = 133
Forward primer  1     AGTGAGGTAGTCCCAACCCA  20
Template        1241  ....................  1260

Reverse primer  1     TCGCAAGGTCTGCATTGTCA  20
Template        1373  ....................  1354


```

Make sure the primer pair has no off target effects

5. Double check primers with refseq accession and/or sequence on NBCI primer blast
```
Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	AGTGAGGTAGTCCCAACCCA	Plus	20	940	959	59.81	55.00	3.00	3.00
Reverse primer	TCGCAAGGTCTGCATTGTCA	Minus	20	1072	1053	60.25	50.00	4.00	3.00
Product length	133
Products on potentially unintended templates
>NM_011609.4 Mus musculus tumor necrosis factor receptor superfamily, member 1a (Tnfrsf1a), mRNA

product length = 133
Forward primer  1     AGTGAGGTAGTCCCAACCCA  20
Template        1241  ....................  1260

Reverse primer  1     TCGCAAGGTCTGCATTGTCA  20
Template        1373  ....................  1354
```


