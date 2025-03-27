
primer design for double cortin like kinase 1 (Dclk1) for mouse mm10 reference that targets the long isoform exon 2 (NOT junction spanning)

1. Navigate to Dclk1 gene for mm10 genome on ucsc genome browser. Note how there are multiple Dclk1 transcripts. Some are long and some are short.

2. Click on the first Dclk1 long isoform transcript to retrieve the ensembl transcript number and refseq accession. The long isoform is often the first transcript in the column (but is not necessarily variant #1).
```
Description: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA. (from RefSeq NM_001195538)
Gencode Transcript: ENSMUST00000196745.4
Gencode Gene: ENSMUSG00000027797.15

RefSeq Accession: NM_001357475.1
```
In the image below note how there are multiple transcripts in the gencode tracks. The top transcript appears to undergo splicing in the first exon, however, the downstream exons are more conserved. To capture all Dclk1 long isoform transcripts, we will make sure that the primers are designed for exon #2.

![Screenshot](https://github.com/p4rkerw/qpcr_design/blob/main/genome.ucsc.edu_cgi-bin_hgTracks_db%3Dmm10%26lastVirtModeType%3Ddefault%26lastVirtModeExtraState%3D%26virtModeType%3Ddefault%26virtMode%3D0%26nonVirtPosition%3D%26position%3Dchr3%253A55242364%252D55248273%26hgsid%3D2497334001_sAOcecptudFNpCatouA6iwzKR2jw%20(2).png)



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


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000196745.4) because other genes that overlap the same region will also have sequences. 
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

This is the sequence for exon 2 only. Note how it starts with an ATG start codon because exon 1 is non-coding. The ensembl transcript identifier also has a _0 at the end.  
```
>mm10_knownGene_ENSMUST00000196745.4_0 range=chr3:55247151-55247526 5'pad=0 3'pad=0 strand=+ repeatMasking=N
ATGTCGTTCGGCAGAGATATGGAGTTGGAGCATTTTGATGAGCGGGACAA
GGCGCAGAGGTACAGCAGGGGGTCCCGTGTGAATGGCCTGCCCAGCCCCA
CACACAGCGCCCACTGCAGCTTCTACCGCACCCGCACCCTGCAGACACTC
AGCTCCGAGAAGAAAGCCAAGAAGGTTCGATTCTACAGAAATGGTGACCG
CTACTTCAAAGGAATTGTGTATGCCATCTCCCCAGACCGCTTCAGATCTT
TCGAGGCCCTGCTGGCTGATTTGACCCGAACTCTCTCGGATAATGTGAAT
TTGCCCCAGGGGGTGAGAACCATCTACACCATCGATGGACTCAAGAAGAT
CTCCAGCCTGGACCAGCTGGTGGAAG
```

4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY   SCORE START   END QSIZE IDENTITY  CHROM  STRAND  START       END   SPAN
------------------------------------------------------------------------------------------------------------
browser new tab details YourSeq   376     1   376   376   100.0%  chr3   +    55247151  55247526    376
browser new tab details YourSeq   125   112   332   376    78.3%  chr3   -    86919794  86920014    221
browser new tab details YourSeq    28   139   175   376    89.2%  chr13  +    74583194  74583286     93
```
Note how there is a high score and 100% match for the region of interest and a partial match for regions on other chromosomes


5. Navigate to NCBI primer blast

Paste the exon 2 sequence into the PCR template box. Unlike ensembl transcripts, Exons do not have unique refseq accession numbers .
Decrease the PCR product maximum size from 1000 to 150

Primer pair specificity checking parameters
Database: Refseq mRNA
Organism: Mus musculus (taxid:10090)

Get Primers

Primer blast will alert you that "Your PCR template is highly similar to the following sequences...." The Dclk1 long isoform undergoes alternative
splicing after transcription that affects a small region of the transcript, which is why some of the isoforms are highly similar. You can check all of the "NM" boxes and proceed. You do not need to check the "XM" predicted
transcript boxes.

```
Accession	Title	Identity	Alignment length	Seq. start	Seq. stop
>NM_001111053.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA	100%	376	409	784
>NM_001357469.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA	100%	376	409	784
XM_036162883.1	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X9, mRNA	100%	376	470	845
XM_017319447.3	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X1, mRNA	100%	376	470	845
XM_006500983.5	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X8, mRNA	100%	376	470	845
XM_006500982.3	PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X7, mRNA	100%	376	470	845
>NM_019978.4	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA	100%	376	409	784
>NM_001357466.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA	100%	376	409	784
>NM_001195538.2	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA	100%	376	409	784
>NM_001357475.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA	100%	376	409	784
```

6. Inspect output of primer search

```
Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	CAGCTCCGAGAAGAAAGCCA	Plus	20	150	169	60.04	55.00	5.00	0.00
Reverse primer	ATCCGAGAGAGTTCGGGTCA	Minus	20	291	272	60.03	55.00	4.00	1.00
Product length	142
Products on intended targets
>NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        558  ....................  577

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        699  ....................  680

>NM_001357469.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        558  ....................  577

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        699  ....................  680

>NM_019978.4 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        558  ....................  577

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        699  ....................  680

>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        558  ....................  577

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        699  ....................  680

>NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        558  ....................  577

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        699  ....................  680

>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        558  ....................  577

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        699  ....................  680

Products on potentially unintended templates
> XM_036162883.1 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X9, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        619  ....................  638

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        760  ....................  741

> XM_017319447.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X1, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        619  ....................  638

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        760  ....................  741

> XM_006500983.5 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X8, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        619  ....................  638

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        760  ....................  741

> XM_006500982.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X7, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        619  ....................  638

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        760  ....................  741

> XM_036154667.1 PREDICTED: Mus musculus microtubule-associated protein 4 (Map4), transcript variant X30, mRNA

product length = 2954
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        3764  A...C.A..A........A.  3783

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        6717  .....TG.-...........  6699

> NM_001205330.2 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 1, mRNA

product length = 3158
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        5296  .....TG.-...........  5278

> XM_030244102.1 PREDICTED: Mus musculus microtubule-associated protein 4 (Map4), transcript variant X9, mRNA

product length = 2939
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        4117  A...C.A..A........A.  4136

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        7055  .....TG.-...........  7037

> NM_001311163.2 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 5, mRNA

product length = 2938
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        1552  A...C.A..A........A.  1571

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        4489  .....TG.-...........  4471

> NM_001420119.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 12, mRNA

product length = 3052
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        5190  .....TG.-...........  5172

> NM_001428296.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 24, mRNA

product length = 2732
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        4870  .....TG.-...........  4852

> XM_036154669.1 PREDICTED: Mus musculus microtubule-associated protein 4 (Map4), transcript variant X42, mRNA

product length = 2732
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        3764  A...C.A..A........A.  3783

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        6495  .....TG.-...........  6477

> NM_001428285.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 14, mRNA

product length = 2938
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        5319  A...C.A..A........A.  5338

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        8256  .....TG.-...........  8238

> XM_017313181.2 PREDICTED: Mus musculus microtubule-associated protein 4 (Map4), transcript variant X36, mRNA

product length = 2825
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        3764  A...C.A..A........A.  3783

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        6588  .....TG.-...........  6570

> NM_001419642.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 7, mRNA

product length = 3161
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        5299  .....TG.-...........  5281

> NM_001428289.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 18, mRNA

product length = 2748
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        4886  .....TG.-...........  4868

> XM_006511962.5 PREDICTED: Mus musculus microtubule-associated protein 4 (Map4), transcript variant X31, mRNA

product length = 2951
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        3764  A...C.A..A........A.  3783

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        6714  .....TG.-...........  6696

> NM_001420118.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 11, mRNA

product length = 2830
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        4968  .....TG.-...........  4950

> NM_001420116.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 9, mRNA

product length = 2845
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        4983  .....TG.-...........  4965

> XM_006511960.4 PREDICTED: Mus musculus microtubule-associated protein 4 (Map4), transcript variant X21, mRNA

product length = 3161
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        3764  A...C.A..A........A.  3783

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        6924  .....TG.-...........  6906

> NM_001420115.1 Mus musculus microtubule-associated protein 4 (Map4), transcript variant 8, mRNA

product length = 2951
Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        2139  A...C.A..A........A.  2158

Forward primer  1     CAGCTCCGAGAAGAAAGCCA  20
Template        5089  .....TG.-...........  5071


```

Make sure that the intended and predicted off targets are what you want. You can search for them using ucsc genome browser. Dont worry about XM predicted transcripts or transcripts with mismatches.

```
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA
>NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA
>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA
>NM_019978.4 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA
>NM_001357469.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA
>NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA
```

All of these are Dclk1 long isoform transcripts, which is what we want.

7. Here are our selected primers
```
>NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA

product length = 142
Forward primer  1    CAGCTCCGAGAAGAAAGCCA  20
Template        558  ....................  577

Reverse primer  1    ATCCGAGAGAGTTCGGGTCA  20
Template        699  ....................  680
```
Use ucsc blat to make sure they align where you expect them to align (ie exon 2). 

Results for forward and reverse primer
```
browser new tab details YourSeq    20     1    20    20   100.0%  chr3   +    55247300  55247319     20

browser new tab details YourSeq    20     1    20    20   100.0%  chr3   -    55247422  55247441     20










