primer design for double cortin like kinase 1 (Dclk1) for mouse mm10 reference that targets the long isoform exon 2 to exon 3 junction

1. Navigate to Dclk1 gene for mm10 genome on ucsc genome browser. Note how there are multiple Dclk1 transcripts. Some are long and some are short.

2. Click on the first Dclk1 long isoform transcript to retrieve the ensembl transcript number and refseq accession. The long isoform is often the first transcript in the column (but is not necessarily variant #1).
```
Description: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA. (from RefSeq NM_001195538)
Gencode Transcript: ENSMUST00000196745.4
Gencode Gene: ENSMUSG00000027797.15

RefSeq Accession: NM_001357475.1
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
One FASTA record per region

Sequnece Formatting Options:
Mask repeats to N


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000196745.4) because other genes that overlap the same region will also have sequences. These are the sequences
for exons 2 and 3
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
>mm10_knownGene_ENSMUST00000196745.4_1 range=chr3:55255865-55256211 5'pad=0 3'pad=0 strand=+ repeatMasking=N
GTGAAAGCTATGTCTGCGGCTCCATCGAGCCCTTTAAGAAGCTGGAGTAC
ACCAAGAATGTGAACCCCAACTGGTCAGTGAACGTCAAGACCACCTCAGC
CTCCCGCGCAGTGTCTTCTTTGGCCACTGCCAAGGGTGGGCCTTCGGAGG
TTCGGGAGAATAAGGATTTCATTCGACCCAAGCTGGTCACCATCATCAGA
AGTGGGGTGAAGCCACGGAAGGCTGTCAGAATCCTGCTGAACAAGAAGAC
GGCTCACTCCTTCGAGCAGGTTCTCACTGACATTACCGACGCTATCAAGC
TGGACTCCGGTGTGGTGAAGCGCCTGTACACTCTGGATGGGAAGCAG
```

We will extract the last two lines of exon 2 and the first two of exon 3 to assemble the exon junction
```
TTGCCCCAGGGGGTGAGAACCATCTACACCATCGATGGACTCAAGAAGAT
CTCCAGCCTGGACCAGCTGGTGGAAG
GTGAAAGCTATGTCTGCGGCTCCATCGAGCCCTTTAAGAAGCTGGAGTAC
ACCAAGAATGTGAACCCCAACTGGTCAGTGAACGTCAAGACCACCTCAGC
```


4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY   SCORE START   END QSIZE IDENTITY  CHROM  STRAND  START       END   SPAN
------------------------------------------------------------------------------------------------------------
browser new tab details YourSeq   175     1   176   176   100.0%  chr3   +    55247451  55255964   8514
browser new tab details YourSeq    48    79   152   176    82.5%  chrX   -   143923354 143923427     74
```
Note how there is a high score and 100% match for the region of interest and a partial match for regions on other chromosomes


4. Navigate to NCBI primer blast
Paste the DNA sequence into the PCR template box
Decrease the PCR product maximum size from 1000 to 150


Primer pair specificity checking parameters
Database: Refseq mRNA
Organism: Mus musculus (taxid:10090)

Get Primers

```
Primer blast will alert you that "Your PCR template is highly similar to the following sequences...." You can check the box next the NM accessions and click submit. 

Download primer pairs 
Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	CCAGCTGGTGGAAGGTGAAA	Plus	20	63	82	60.18	55.00	8.00	0.00
Reverse primer	CTGACCAGTTGGGGTTCACA	Minus	20	154	135	59.82	55.00	4.00	1.00
Product length	92
Products on intended targets
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        771  ....................  790

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        862  ....................  843

>NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        771  ....................  790

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        862  ....................  843

>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        771  ....................  790

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        862  ....................  843

>NM_019978.4 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        771  ....................  790

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        862  ....................  843

>NM_001357469.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        771  ....................  790

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        862  ....................  843

>NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        771  ....................  790

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        862  ....................  843

Products on potentially unintended templates
> XM_006500982.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X7, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        832  ....................  851

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        923  ....................  904

> XM_006500983.5 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X8, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        832  ....................  851

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        923  ....................  904

> XM_017319447.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X1, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        832  ....................  851

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        923  ....................  904

> XM_036162883.1 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X9, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        832  ....................  851

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        923  ....................  904

> XM_006501462.5 PREDICTED: Mus musculus Fras1 related extracellular matrix protein 2 (Frem2), transcript variant X2, mRNA

product length = 3425
Forward primer  1     CCAGCTGGTGGAAGGTGAAA  20
Template        6093  .A.C.......TCA......  6112

Reverse primer  1     CTGACCAGTTGGGGTTCACA  20
Template        9517  T......T.CT........T  9498

> XM_006515616.4 PREDICTED: Mus musculus ATP-binding cassette, sub-family D member 4 (Abcd4), transcript variant X8, mRNA

product length = 51
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        188  .G........CC..C....G  207

Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        238  A....A...T.C.......C  219

> XM_030249522.2 PREDICTED: Mus musculus mannosidase 2, alpha 1 (Man2a1), transcript variant X1, mRNA

product length = 2566
Forward primer  1     CCAGCTGGTGGAAGGTGAAA  20
Template        1472  ....A.......GTT..G..  1491

Reverse primer  1     CTGACCAGTTGGGGTTCACA  20
Template        4037  T.......A...ATA.....  4018

> NM_008549.2 Mus musculus mannosidase 2, alpha 1 (Man2a1), mRNA

product length = 2738
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        511  ....A.......GTT..G..  530

Reverse primer  1     CTGACCAGTTGGGGTTCACA  20
Template        3248  T.......A...ATA.....  3229

> XM_006515617.5 PREDICTED: Mus musculus ATP-binding cassette, sub-family D member 4 (Abcd4), transcript variant X9, mRNA

product length = 51
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        181  .G........CC..C....G  200

Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        231  A....A...T.C.......C  212




```

Make sure the primer pair has no off target effects. In this case, it appears as though there are unintended templates that target other transcripts. However, if you look at the location of the primers here https://github.com/p4rkerw/qpcr_design/blob/main/www.ncbi.nlm.nih.gov_tools_primer-blast_primertool.cgi_ctg_time%3D1743016255%26job_key%3DUliMoYAVjb2qg4iGheastP_9vYbS7qab0w%26CheckStatus%3DCheck.png
you can see that they all target the exon2-exon3 junction of Dclk1. This is the desired region because this junction is not present in the Dclk1 short isoforms. Importantly, this primer set will only quantify mature spliced Dclk1 long isoforms


Targeted transcripts:
```
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA
>NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA
>NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA
>NM_019978.4 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA
>NM_001357469.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA
>NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA

```



Here are the primers for our target
```

Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	CCAGCTGGTGGAAGGTGAAA	Plus	20	63	82	60.18	55.00	8.00	0.00
Reverse primer	CTGACCAGTTGGGGTTCACA	Minus	20	154	135	59.82	55.00	4.00	1.00
Product length	92
Products on intended targets
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 92
Forward primer  1    CCAGCTGGTGGAAGGTGAAA  20
Template        771  ....................  790

Reverse primer  1    CTGACCAGTTGGGGTTCACA  20
Template        862  ....................  843
```

5. Double check primers with refseq accession on NBCI primer blast or ucsc in-silico pcr tool. You cant use blat to search for these primers because they span a junction. In other words, these sequences are only present in cDNA (spliced mature mRNA). 

```
	The sequences and coordinates shown below are from GENCODE Genes, not from the genome assembly. The links lead to the Genome Browser at the position of the entire target sequence.
>ENSMUST00000167204.7__Dclk1:609+700 92bp CCAGCTGGTGGAAGGTGAAA CTGACCAGTTGGGGTTCACA
CCAGCTGGTGGAAGGTGAAAgctatgtctgcggctccatcgagcccttta
agaagctggagtacaccaagaaTGTGAACCCCAACTGGTCAG

>ENSMUST00000198154.1__Dclk1:235+326 92bp CCAGCTGGTGGAAGGTGAAA CTGACCAGTTGGGGTTCACA
CCAGCTGGTGGAAGGTGAAAgctatgtctgcggctccatcgagcccttta
agaagctggagtacaccaagaaTGTGAACCCCAACTGGTCAG

>ENSMUST00000054237.13__Dclk1:609+700 92bp CCAGCTGGTGGAAGGTGAAA CTGACCAGTTGGGGTTCACA
CCAGCTGGTGGAAGGTGAAAgctatgtctgcggctccatcgagcccttta
agaagctggagtacaccaagaaTGTGAACCCCAACTGGTCAG

>ENSMUST00000196745.4__Dclk1:771+862 92bp CCAGCTGGTGGAAGGTGAAA CTGACCAGTTGGGGTTCACA
CCAGCTGGTGGAAGGTGAAAgctatgtctgcggctccatcgagcccttta
agaagctggagtacaccaagaaTGTGAACCCCAACTGGTCAG


```

