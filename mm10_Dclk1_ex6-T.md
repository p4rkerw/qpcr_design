
primer design for double cortin like kinase 1 (Dclk1) for mouse mm10 reference that targets both short isoform exon 2 and long isoform exon 6 (NOT junction spanning)

1. Navigate to Dclk1 gene for mm10 genome on ucsc genome browser. Note how there are multiple Dclk1 transcripts. Some are long and some are short.

2. Click on the second Dclk1 short isoform transcript to retrieve the ensembl transcript number and refseq accession (Dont click on the ultrashort isoform). 
```
Description: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 7, mRNA. (from RefSeq NM_001195540)
Gencode Transcript: ENSMUST00000070418.8
Gencode Gene: ENSMUSG00000027797.15

RefSeq Accession: NM_001111052.2
```

3. Retrieve the whole gene DNA sequence of the gene using the Table Browser tool
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
One FASTA record per region (exon, intron, etc)

Sequence Formatting Options:
Mask repeats to N


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000070418.8) because other genes that overlap the same region will also have sequences. 
This is the sequence for the entire gene:
```
>mm10_knownGene_ENSMUST00000196745.4 range=chr3:55247151-55533734 5'pad=0 3'pad=0 strand=+ repeatMasking=N
ATGTCGTTCGGCAGAGATATGGAGTTGGAGCATTTTGATGAGCGGGACAA
GGCGCAGAGGTACAGCAGGGGGTCCCGTGTGAATGGCCTGCCCAGCCCCA
CACACAGCGCCCACTGCAGCTTCTACCGCACCCGCACCCTGCAGACACTC
AGCTCCGAGAAGAAAGCCAAGAAGGTTCGATTCTACAGAAATGGTGACCG
CTACTTCAAAGGAATTGTGTATGCCATCTCCCCAGACCGCTTCAGATCTT
TCGAGGCCCTGCTGGCTGATTTGACCCGAACTCTCTCGGATAATGTGAAT
TTGCCCCAGGGGGTGAGAACCATCTACACCATCGATGGACTCAAGAAGAT
CTCCAGCCTGGACCAGCTGGTGGAAGGTGAAAGCTATGTCTGCGGCTCCA
TCGAGCCCTTTAAGAAGCTGGAGTACACCAAGAATGTGAACCCCAACTGG
TCAGTGAACGTCAAGACCACCTCAGCCTCCCGCGCAGTGTCTTCTTTGGC
CACTGCCAAGGGTGGGCCTTCGGAGGTTCGGGAGAATAAGGATTTCATTC
GACCCAAGCTGGTCACCATCATCAGAAGTGGGGTGAAGCCACGGAAGGCT
GTCAGAATCCTGCTGAACAAGAAGACGGCTCACTCCTTCGAGCAGGTTCT
CACTGACATTACCGACGCTATCAAGCTGGACTCCGGTGTGGTGAAGCGCC
TGTACACTCTGGATGGGAAGCAGGTGATGTGCCTTCAGGACTTTTTTGGT
GACGATGACATTTTTATTGCATGTGGACCAGAGAAGTTCCGTTACCAGGA
TGATTTCTTGCTAGATGAAAGTGAATGTCGAGTGGTGAAATCAACTTCTT
ACACCAAAATAGCATCAGCGTCCCGCAGAGGCACAACCAAGAGCCCAGGA
CCTTCCCGGAGAAGCAAGTCCCCAGCCTCCACCAGCTCAGTTAATGGAAC
CCCTGGTAGTCAGCTCTCTACTCCACGCTCGGGCAAGTCACCAAGTCCAT
CACCCACCAGCCCAGGAAGCCTGCGGAAGCAGAGGATCTCTCAGCATGGC
GGCTCCTCGACTTCACTTTCATCCACTAAAGTTTGCAGCTCAATGGATGA
GAATGATGGCCCTGGGGAAGAAGAGTCTGAGGAAGGCTTCCAGATTCCTG
CCACAATAACAGAGAGATACAAAGTCGGGAGAACAATAGGAGACGGAAAT
TTTGCTGTTGTCAAGGAATGTATAGAGAGGTCGACTGCTCGGGAGTATGC
CCTGAAAATCATCAAGAAAAGCAAATGCCGAGGCAAAGAGCACATGATCC
AGAACGAGGTCTCCATCCTACGGAGGGTGAAGCACCCCAACATTGTCCTC
CTGATTGAAGAGATGGATGTGCCGACTGAACTGTATCTTGTAATGGAATT
AGTGAAGGGTGGAGACCTTTTCGATGCCATCACCTCCACTAGCAAATACA
CAGAGAGAGATGCCAGCGGGATGCTGTACAACCTGGCCAGCGCCATCAAA
TACCTGCACAGCCTGAACATCGTCCACCGTGACATCAAGCCAGAGAATCT
GCTGGTGTATGAGCACCAGGATGGCAGTAAGTCACTCAAGTTGGGTGACT
TTGGCCTGGCCACAATTGTCGACGGCCCCCTGTACACAGTCTGTGGCACC
CCAACATATGTGGCTCCAGAAATCATTGCAGAGACTGGATATGGCCTCAA
GGTGGACATCTGGGCAGCTGGCGTGATCACTTATATCCTGCTGTGTGGCT
TCCCTCCGTTCCGTGGTGGGGATGACCAGGAGGTGCTTTTTGACCAGATC
TTGATGGGCCAAGTGGACTTTCCATCTCCGTATTGGGACAATGTGTCAGA
TTCTGCTAAGGAGCTCATCAACATGATGCTGTTGGTTAACGTGGACCAGA
GATTTTCAGCCGTGCAGGTCCTTGAGCATCCCTGGGTTAATGATGATGGT
CTCCCAGAAAATGAGCATCAGCTGTCAGTAGCTGGCAAAATCAAGAAGCA
TTTCAACACAGGCCCCAAGCCGAGCAGCACTGCAGCAGGAGTTTCTGTAA
TAGCAACCACCGCTCTTGATAAGGAGAGGCAGGTTTTCCGACGAAGACGC
AACCAGGATGTGAGGAGCCGGTACAAGGCGCAGCCAGCTCCACCGGAATT
GAACTCGGAATCGGAGGACTACTCCCCCAGCTCCTCTGAGACTGTTCGCT
CCCCCAATTCGCCCTTTTAA
```

Short isoform exon 1 is poorly conserved between transcripts so we will use short isoform 2 sequence, which is the same as long isoform 6.

```
>mm10_knownGene_ENSMUST00000070418.8_1 range=chr3:55463001-55463095 5'pad=0 3'pad=0 strand=+ repeatMasking=N
TTAATGGAACCCCTGGTAGTCAGCTCTCTACTCCACGCTCGGGCAAGTCA
CCAAGTCCATCACCCACCAGCCCAGGAAGCCTGCGGAAGCAGAGG
```

4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY   SCORE START   END QSIZE IDENTITY  CHROM  STRAND  START       END   SPAN
------------------------------------------------------------------------------------------------------------
browser new tab details YourSeq    95     1    95    95   100.0%  chr3   +    55463001  55463095     95
```
Note how there is a high score and 100% match for the region of interest and a partial match for regions on other chromosomes


5. Navigate to NCBI primer blast

Paste the sequence into the PCR template box. 
Decrease the PCR product maximum size from 1000 to 150

Primer pair specificity checking parameters
Database: Refseq mRNA
Organism: Mus musculus (taxid:10090)

Get Primers

Primer blast will alert you that "Your PCR template is highly similar to the following sequences...." We chose a region that should be shared by all Dclk1 isoforms so this is what we expected. You can check all of the "NM" boxes and proceed. You do not need to check the "XM" predicted transcript boxes.

```
>NM_001357476.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 13, mRNA	100%	95	356	450
>NM_001111053.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA	100%	95	1349	1443
>NM_001195540.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 7, mRNA	100%	95	356	450
>NM_001357469.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA	100%	95	1349	1443
>XM_030252412.2	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X6, mRNA	100%	95	364	458
>NM_001357468.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 10, mRNA	100%	95	356	450
>XM_006500981.5	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X2, mRNA	100%	95	363	457
>XM_030252411.2	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X4, mRNA	100%	95	360	454
>XM_036162883.1	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X9, mRNA	100%	95	1410	1504
>XM_017319447.3	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X1, mRNA	100%	95	1410	1504
>XM_006500983.5	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X8, mRNA	100%	95	1410	1504
>XM_006500982.3	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X7, mRNA	100%	95	1410	1504
>NM_019978.4	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA	100%	95	1349	1443
>NM_001111052.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 3, mRNA	100%	95	356	450
>XM_036162882.1	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X5, mRNA	100%	95	142	236
>NM_001357466.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA	100%	95	1349	1443
>NM_001195539.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 6, mRNA	100%	95	356	450
>NM_001195538.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA	100%	95	1349	1443
>NM_001111051.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 2, mRNA	100%	95	356	450
>NM_001357475.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA	100%	95	1349	1443

```

6. Inspect output of primer search

```
Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	TCAGCTCTCTACTCCACGCT	Plus	20	20	39	60.03	55.00	4.00	0.00
Reverse primer	CTCTGCTTCCGCAGGCTT	Minus	18	94	77	60.05	61.11	4.00	2.00
Product length	75
Products on intended targets
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1442  ..................  1425

>NM_001111051.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 2, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        375  ....................  394

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        449  ..................  432

>NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1442  ..................  1425

>NM_001195539.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 6, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        375  ....................  394

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        449  ..................  432

>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1442  ..................  1425

>NM_001111052.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 3, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        375  ....................  394

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        449  ..................  432

>NM_019978.4 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1442  ..................  1425

>NM_001357468.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 10, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        375  ....................  394

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        449  ..................  432

>NM_001357469.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1442  ..................  1425

>NM_001195540.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 7, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        375  ....................  394

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        449  ..................  432

>NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1442  ..................  1425

>NM_001357476.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 13, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        375  ....................  394

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        449  ..................  432

Products on potentially unintended templates
> XM_036162882.1 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X5, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        161  ....................  180

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        235  ..................  218

> XM_006500982.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X7, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1429  ....................  1448

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1503  ..................  1486

> XM_006500983.5 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X8, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1429  ....................  1448

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1503  ..................  1486

> XM_017319447.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X1, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1429  ....................  1448

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1503  ..................  1486

> XM_036162883.1 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X9, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1429  ....................  1448

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1503  ..................  1486

> XM_030252411.2 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X4, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        379  ....................  398

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        453  ..................  436

> XM_006500981.5 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X2, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        382  ....................  401

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        456  ..................  439

> XM_030252412.2 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X6, mRNA

product length = 75
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        383  ....................  402

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        457  ..................  440

> NM_001195540.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 7, mRNA

product length = 3452
Forward primer  1    TCAGCTCTCTACTCCACGCT  20
Template        375  ....................  394

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        3826  TA.......AT......A  3809

> NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA

product length = 3452
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        4819  TA.......AT......A  4802

> NM_001037764.1 Mus musculus retinoic acid induced 1 (Rai1), transcript variant 2, mRNA

product length = 589
Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        3203  ...A.G.A.A........  3186

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        2615  ........G.ATG.....  2632


product length = 3851
Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        6465  .C.A.TC...T.......  6448

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        2615  ........G.ATG.....  2632

> NM_009021.2 Mus musculus retinoic acid induced 1 (Rai1), transcript variant 1, mRNA

product length = 589
Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        3426  ...A.G.A.A........  3409

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        2838  ........G.ATG.....  2855


product length = 3851
Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        6688  .C.A.TC...T.......  6671

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        2838  ........G.ATG.....  2855

> NM_001167883.1 Mus musculus ankyrin repeat domain 50 (Ankrd50), transcript variant 2, mRNA

product length = 203
Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1435  AAA.........T..G..  1418

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1233  G.....A..GC.......  1250

> XM_006535582.5 PREDICTED: Mus musculus ankyrin repeat domain 50 (Ankrd50), transcript variant X1, mRNA

product length = 203
Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1058  AAA.........T..G..  1041

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        856  G.....A..GC.......  873

> NM_008429.3 Mus musculus potassium inwardly-rectifying channel, subfamily J, member 9 (Kcnj9), transcript variant 2, mRNA

product length = 1218
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1947  C.T....C...AG.......  1928

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        730  TG.....G.T.......A  747

> NM_001360808.1 Mus musculus potassium inwardly-rectifying channel, subfamily J, member 9 (Kcnj9), transcript variant 1, mRNA

product length = 1218
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1977  C.T....C...AG.......  1958

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        760  TG.....G.T.......A  777

> XM_011250460.4 PREDICTED: Mus musculus avian reticuloendotheliosis viral (v-rel) oncogene related B (Relb), transcript variant X4, mRNA

product length = 1621
Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        2576  ..G..G.CT.C.......  2559

Reverse primer  1    CTCTGCTTCCGCAGGCTT  18
Template        956  GCT.......C.T.....  973

> XM_036162443.1 PREDICTED: Mus musculus spectrin beta, non-erythrocytic 5 (Sptbn5), transcript variant X1, mRNA

product length = 1159
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        4857  C....A.CA.......G...  4876

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        6015  TG.....G.A.......C  5998


```

Make sure that the intended and predicted off targets are what you want. You can search for them using ucsc genome browser. Dont worry about XM predicted transcripts or transcripts with mismatches.

```
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA
>NM_001111051.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 2, mRNA
>NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA
>NM_001195539.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 6, mRNA
>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA
>NM_001111052.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 3, mRNA
>NM_019978.4 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA
>NM_001357468.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 10, mRNA
>NM_001357469.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA
>NM_001195540.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 7, mRNA
>NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA
>NM_001357476.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 13, mRNA

```

These are both short and long Dclk1 transcripts, which is what we want. 

7. Here are our selected primers.  
```
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	TCAGCTCTCTACTCCACGCT	Plus	20	20	39	60.03	55.00	4.00	0.00
Reverse primer	CTCTGCTTCCGCAGGCTT	Minus	18	94	77	60.05	61.11	4.00	2.00
Product length	75
Products on intended targets
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 75
Forward primer  1     TCAGCTCTCTACTCCACGCT  20
Template        1368  ....................  1387

Reverse primer  1     CTCTGCTTCCGCAGGCTT  18
Template        1442  ..................  1425
```
Use ucsc in-silico pcr tool to make sure they align where you expect them to align (ie an exon shared by both short and long isoforms).

Results for forward and reverse primer
```

>chr3:55463020+55463094 75bp TCAGCTCTCTACTCCACGCT CTCTGCTTCCGCAGGCTT
TCAGCTCTCTACTCCACGCTcgggcaagtcaccaagtccatcacccacca
gcccaggAAGCCTGCGGAAGCAGAG








