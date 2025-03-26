primer design for double cortin like kinase 1 (Dclk1) for mouse mm10 reference that targets the short and long isoforms 

1. Navigate to Dclk1 gene for mm10 genome on ucsc genome browser. Note how there are multiple Dclk1 transcripts. Some are long and some are short.

2. Click on the first Dclk1 long isoform transcript to retrieve the ensembl transcript number and refseq accession. The short isoform is transcribed from an alternative promoter
located near chr3:55,461,758 downstream of the long isoform promoter. Do not confuse it with the ultra short transcript, which has fewer exons
```
Description: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 3, mRNA. (from RefSeq NM_001111052)
Gencode Transcript: ENSMUST00000070418.8
Gencode Gene: ENSMUSG00000027797.15

RefSeq Accession: NM_001111052.2
```

3. Retrieve the DNA sequence of the gene using the Table Browser tool. Make sure to use the coordinates of the desired isoform chr3:55,461,758-55,539,064
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


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000070418.8) because other genes that overlap the same region will also have sequences. 
```
>mm10_knownGene_ENSMUST00000070418.8 range=chr3:55462064-55533627 5'pad=0 3'pad=0 strand=+ repeatMasking=N
ATGTTAGAGCTCATAGAAGTTAATGGAACCCCTGGTAGTCAGCTCTCTAC
TCCACGCTCGGGCAAGTCACCAAGTCCATCACCCACCAGCCCAGGAAGCC
TGCGGAAGCAGAGGATCTCTCAGCATGGCGGCTCCTCGACTTCACTTTCA
TCCACTAAAGTTTGCAGCTCAATGGATGAGAATGATGGCCCTGGGGAAGA
AGAGTCTGAGGAAGGCTTCCAGATTCCTGCCACAATAACAGAGAGATACA
AAGTCGGGAGAACAATAGGAGACGGAAATTTTGCTGTTGTCAAGGAATGT
ATAGAGAGGTCGACTGCTCGGGAGTATGCCCTGAAAATCATCAAGAAAAG
CAAATGCCGAGGCAAAGAGCACATGATCCAGAACGAGGTCTCCATCCTAC
GGAGGGTGAAGCACCCCAACATTGTCCTCCTGATTGAAGAGATGGATGTG
CCGACTGAACTGTATCTTGTAATGGAATTAGTGAAGGGTGGAGACCTTTT
CGATGCCATCACCTCCACTAGCAAATACACAGAGAGAGATGCCAGCGGGA
TGCTGTACAACCTGGCCAGCGCCATCAAATACCTGCACAGCCTGAACATC
GTCCACCGTGACATCAAGCCAGAGAATCTGCTGGTGTATGAGCACCAGGA
TGGCAGTAAGTCACTCAAGTTGGGTGACTTTGGCCTGGCCACAATTGTCG
ACGGCCCCCTGTACACAGTCTGTGGCACCCCAACATATGTGGCTCCAGAA
ATCATTGCAGAGACTGGATATGGCCTCAAGGTGGACATCTGGGCAGCTGG
CGTGATCACTTATATCCTGCTGTGTGGCTTCCCTCCGTTCCGTGGAAGTG
GGGATGACCAGGAGGTGCTTTTTGACCAGATCTTGATGGGCCAAGTGGAC
TTTCCATCTCCGTATTGGGACAATGTGTCAGATTCTGCTAAGGAGCTCAT
CAACATGATGCTGTTGGTTAACGTGGACCAGAGATTTTCAGCCGTGCAGG
TCCTTGAGCATCCCTGGGTTAATGATGATGGTCTCCCAGAAAATGAGCAT
CAGCTGTCAGTAGCTGGCAAAATCAAGAAGCATTTCAACACAGGCCCCAA
GCCGAGCAGCACTGCAGCAGGAGTTTCTGTAATAGCACTGGACCACGGGT
TTACCATCAAGAGATCAGGGTCTTTGGACTACTACCAACAACCAGGAATG
TATTGGATAAGACCACCGCTCTTGATAAGGAGAGGCAGGTTTTCCGACGA
AGACGCAACCAGGATGTGA

```

4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY   SCORE START   END QSIZE IDENTITY  CHROM  STRAND  START       END   SPAN
------------------------------------------------------------------------------------------------------------
browser new tab details YourSeq  1240    18  1269  1269   100.0%  chr3   +    55462999  55533627  70629
browser new tab details YourSeq    48   580   637  1269    91.4%  chr3   -    86805580  86805637     58
browser new tab details YourSeq    32  1009  1042  1269   100.0%  chr13  -   111224618 111225013    396
browser new tab details YourSeq    26   876   911  1269    82.8%  chr12  +    30745710  30745742     33
browser new tab details YourSeq    25  1106  1131  1269   100.0%  chr12  -     4718998   4719025     28
browser new tab details YourSeq    23   776   800  1269    96.0%  chr10  +    80126336  80126360     25
browser new tab details YourSeq    22   335   359  1269    96.0%  chr11  -    51097991  51098021     31
```
Note how there is a high score and 100% match for the region of interest and a partial match for regions on other chromosomes


4. Navigate to NCBI primer blast
Paste the refseq accession NM_001111052.2 into the PCR template box
Decrease the PCR product maximum size from 1000 to 150

Exon/intron selection
> Exon junction span: Primer must span an exon-exon junction

Primer pair specificity checking parameters
Database: Refseq mRNA
Organism: Mus musculus (taxid:10090)

Get Primers

```
Primer blast will alert you that "Your PCR template is highly similar to the following sequences...."
```
>NM_001357476.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 13, mRNA	99.96%	7060	1	7057
>NM_001357466.1	Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA	100%	6707	1347	8053
```
You can check the boxes next to these accessions and click submit. These transcripts are highly similar to NM_001111052.2 as shown by the 99.96% and 100% identity match. The Dclk1 short isoform undergoes alternative
splicing after transcription that affects a small region of the transcript, which is why there are highly similar isoforms.

```

```
Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	CAGAGGATCTCTCAGCATGGC	Plus	21	445	465	60.27	57.14	6.00	2.00
Reverse primer	TCCTCAGACTCTTCTTCCCCA	Minus	21	548	528	59.57	52.38	5.00	0.00
Product length	104
Exon junction	535/536 (reverse primer) on template NM_001111052.2
Products on intended targets
>NM_001111052.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 3, mRNA

product length = 104
Forward primer  1    CAGAGGATCTCTCAGCATGGC  21
Template        445  .....................  465

Reverse primer  1    TCCTCAGACTCTTCTTCCCCA  21
Template        548  .....................  528

>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA

product length = 104
Forward primer  1     CAGAGGATCTCTCAGCATGGC  21
Template        1438  .....................  1458

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        1541  .....................  1521

Products on potentially unintended templates
> NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA

product length = 104
Forward primer  1     CAGAGGATCTCTCAGCATGGC  21
Template        1438  .....................  1458

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        1541  .....................  1521

> NM_001111051.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 2, mRNA

product length = 104
Forward primer  1    CAGAGGATCTCTCAGCATGGC  21
Template        445  .....................  465

Reverse primer  1    TCCTCAGACTCTTCTTCCCCA  21
Template        548  .....................  528

> NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 104
Forward primer  1     CAGAGGATCTCTCAGCATGGC  21
Template        1438  .....................  1458

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        1541  .....................  1521

> XM_036162882.1 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X5, mRNA

product length = 104
Forward primer  1    CAGAGGATCTCTCAGCATGGC  21
Template        313  TGT.T................  333

Reverse primer  1    TCCTCAGACTCTTCTTCCCCA  21
Template        416  .....................  396

> XM_030252412.2 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X6, mRNA

product length = 104
Forward primer  1    CAGAGGATCTCTCAGCATGGC  21
Template        530  .GAT.T...............  550

Reverse primer  1    TCCTCAGACTCTTCTTCCCCA  21
Template        633  .....................  613

> XM_030252411.2 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X4, mRNA

product length = 104
Forward primer  1    CAGAGGATCTCTCAGCATGGC  21
Template        526  .GAT.T...............  546

Reverse primer  1    TCCTCAGACTCTTCTTCCCCA  21
Template        629  .....................  609

> XM_017313709.2 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X5, mRNA

product length = 792
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3150  .......T.C...........  3130

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2359  ...C.......AG.C.....C  2379

> XM_006511578.5 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X4, mRNA

product length = 792
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3159  .......T.C...........  3139

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2368  ...C.......AG.C.....C  2388

> XM_006511582.4 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X9, mRNA

product length = 819
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3189  .......T.C...........  3169

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2371  ...C.......AG.C.....C  2391

> XM_011242841.4 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X2, mRNA

product length = 819
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3183  .......T.C...........  3163

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2365  ...C.......AG.C.....C  2385

> XM_006511583.5 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X8, mRNA

product length = 819
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3239  .......T.C...........  3219

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2421  ...C.......AG.C.....C  2441

> XM_030244747.2 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X12, mRNA

product length = 819
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3217  .......T.C...........  3197

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2399  ...C.......AG.C.....C  2419

> XM_006511584.4 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X10, mRNA

product length = 819
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3069  .......T.C...........  3049

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2251  ...C.......AG.C.....C  2271

> NM_001421569.1 Mus musculus ring finger 111 (Rnf111), transcript variant 7, mRNA

product length = 768
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3164  .......T.C...........  3144

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2397  ...C.......AG.C.....C  2417

> XM_006511576.3 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X1, mRNA

product length = 819
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3186  .......T.C...........  3166

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2368  ...C.......AG.C.....C  2388

> NM_033604.3 Mus musculus ring finger 111 (Rnf111), transcript variant 1, mRNA

product length = 792
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3191  .......T.C...........  3171

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2400  ...C.......AG.C.....C  2420

> XM_030244746.2 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X11, mRNA

product length = 819
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3236  .......T.C...........  3216

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2418  ...C.......AG.C.....C  2438

> NM_001421565.1 Mus musculus ring finger 111 (Rnf111), transcript variant 4, mRNA

product length = 795
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3243  .......T.C...........  3223

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2449  ...C.......AG.C.....C  2469

> XM_006511581.5 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X7, mRNA

product length = 768
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3126  .......T.C...........  3106

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2359  ...C.......AG.C.....C  2379

> XM_006511577.4 PREDICTED: Mus musculus ring finger 111 (Rnf111), transcript variant X3, mRNA

product length = 795
Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        3162  .......T.C...........  3142

Reverse primer  1     TCCTCAGACTCTTCTTCCCCA  21
Template        2368  ...C.......AG.C.....C  2388
```


Make sure the primer pair has no off target effects. In this case, it appears as though there are unintended templates that target other transcripts. However, the unintended targets represent additional Dclk1 isoforms.
The Dclk1 transcripts targeted by this primer pair include # 3, 9, 5, 2 and 12. You can figure out which are short and long isoforms by looking at the ucsc browser refseq track or searching for the accessions.
Here is the transcripts info, refseq accessions and predicted isoform targets
```
>NM_001111052.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 3, mRNA - SHORT
>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA - LONG
> NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA - LONG
> NM_001111051.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 2, mRNA - SHORT
> NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA - LONG
```
In summary, these primer pairs measure both short and long isoforms because there is no unique sequence on the short isoform that does not also capture the long isoform. In this way, the primers are measuring total Dclk1.


Here are the primers for our target
```
>NM_001111052.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 3, mRNA

product length = 104
Forward primer  1    CAGAGGATCTCTCAGCATGGC  21
Template        445  .....................  465

Reverse primer  1    TCCTCAGACTCTTCTTCCCCA  21
Template        548  .....................  528
```

5. Double check primers with refseq accession on NBCI primer blast



