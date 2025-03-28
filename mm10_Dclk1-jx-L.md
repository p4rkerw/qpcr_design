primer design for double cortin like kinase 1 (Dclk1) for mouse mm10 reference that targets a long isoform exon-exon junction.

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
One FASTA record per gene

Sequnece Formatting Options:
Mask repeats to N


Make sure that the DNA sequence you copy matches the ensembl transcript (ENSMUST00000196745.4) because other genes that overlap the same region will also have sequences. 
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

4. Navigate to UCSC BLAT to check specificity of the sequence https://genome.ucsc.edu/cgi-bin/hgBlat
Genome: Mouse
Assembly: Dec.2011 (GRCm38/mm10)

```
   ACTIONS                 QUERY   SCORE START   END QSIZE IDENTITY  CHROM  STRAND  START       END   SPAN
------------------------------------------------------------------------------------------------------------
browser new tab details YourSeq  2205     1  2220  2220   100.0%  chr3   +    55247151  55533734 286584
browser new tab details YourSeq   271   112  1558  2220    81.6%  chr3   -    86805580  86920014 114435
browser new tab details YourSeq   107   379   659  2220    78.2%  chrX   -   143923153 143923427    275
browser new tab details YourSeq    25  2024  2049  2220   100.0%  chr12  -     4718998   4719025     28
browser new tab details YourSeq    25  2172  2197  2220   100.0%  chr11  -    82023262  82023292     31
browser new tab details YourSeq    25  1127  1155  2220    96.3%  chr1   +   104791883 104791916     34
browser new tab details YourSeq    23  1843  1870  2220    80.8%  chr2   -    33692626  33692651     26
browser new tab details YourSeq    23  1059  1083  2220   100.0%  chr3   +   110459741 110459767     27
browser new tab details YourSeq    22  1256  1280  2220    96.0%  chr11  -    51097991  51098021     31
browser new tab details YourSeq    20   796   815  2220   100.0%  chr10  -    14959027  14959046     20
```
Note how there is a high score and 100% match for the region of interest and a partial match for regions on other chromosomes


4. Navigate to NCBI primer blast
Paste the refseq accession NM_001357475.1 into the PCR template box
Decrease the PCR product maximum size from 1000 to 150

Exon/intron selection
> Exon junction span: Primer must span an exon-exon junction

Primer pair specificity checking parameters
Database: Refseq mRNA
Organism: Mus musculus (taxid:10090)

Get Primers

```
Primer blast will alert you that "Your PCR template is highly similar to the following sequences....", including NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA
You can check the box next to this accession and click submit. This transcript is highly similar to NM_001357475.1 as shows by the 99.96% identity match. The Dclk1 long isoform undergoes alternative
splicing after transcription that affects a small region of the transcript, which is why some of the isoforms are highly similar.



Primer pair 1
Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	ATCAGTGCACTAGCGGTCG	Plus	19	269	287	59.86	57.89	8.00	2.00
Reverse primer	CTTGCTTATGGAACCGGTCG	Minus	20	402	383	58.99	55.00	6.00	2.00
Product length	134
Exon junction	388/389 (reverse primer) on template NM_001357475.1
Products on intended targets
>NM_001195538.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 5, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        269  ...................  287

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        402  ....................  383

>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        269  ...................  287

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        402  ....................  383

Products on potentially unintended templates
> NM_001111053.2 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 4, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        269  ...................  287

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        402  ....................  383

> NM_001357469.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 11, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        269  ...................  287

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        402  ....................  383

> XM_036162883.1 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X9, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        330  ...................  348

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        463  ....................  444

> XM_017319447.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X1, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        330  ...................  348

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        463  ....................  444

> XM_006500983.5 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X8, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        330  ...................  348

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        463  ....................  444

> XM_006500982.3 PREDICTED: Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant X7, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        330  ...................  348

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        463  ....................  444

> NM_019978.4 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 1, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        269  ...................  287

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        402  ....................  383

> NM_001357466.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 9, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        269  ...................  287

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        402  ....................  383
```

Make sure the primer pair has no off target effects. In this case, it appears as though there are unintended templates that target other transcripts. However, if you look at the location of the primers here https://github.com/p4rkerw/qpcr_design/blob/main/www.ncbi.nlm.nih.gov_tools_primer-blast_primertool.cgi_ctg_time%3D1743016255%26job_key%3DUliMoYAVjb2qg4iGheastP_9vYbS7qab0w%26CheckStatus%3DCheck.png
you can see that they all target the exon1-exon2 junction of Dclk1. This is the desired region because exon 1 is not present in the Dclk1 short isoforms. Importantly, this primer set will only quantify mature spliced Dclk1 long isoforms for transcript variants 12, 4, 11, 1, 9, and 5.

Here are the primers for our target
```
>NM_001357475.1 Mus musculus doublecortin-like kinase 1 (Dclk1), transcript variant 12, mRNA

product length = 134
Forward primer  1    ATCAGTGCACTAGCGGTCG  19
Template        269  ...................  287

Reverse primer  1    CTTGCTTATGGAACCGGTCG  20
Template        402  ....................  383
```

5. Double check primers with refseq accession on NBCI primer blast. You cant use blat to search for these primers because they span a junction. In other words, these sequences are only present in cDNA (spliced mature mRNA). An alternative is the ucsc in-silico primer tool. 

```
	The sequences and coordinates shown below are from GENCODE Genes, not from the genome assembly. The links lead to the Genome Browser at the position of the entire target sequence.
>ENSMUST00000167204.7__Dclk1:107+240 134bp ATCAGTGCACTAGCGGTCG CTTGCTTATGGAACCGGTCG
ATCAGTGCACTAGCGGTCGcagcttccagacgctcgtgctccgcagcccc
agccgcgcccagcccggcgaggacagctccagcagccggccacagacaac
ccagcctccacccgCGACCGGTTCCATAAGCAAG

>ENSMUST00000054237.13__Dclk1:107+240 134bp ATCAGTGCACTAGCGGTCG CTTGCTTATGGAACCGGTCG
ATCAGTGCACTAGCGGTCGcagcttccagacgctcgtgctccgcagcccc
agccgcgcccagcccggcgaggacagctccagcagccggccacagacaac
ccagcctccacccgCGACCGGTTCCATAAGCAAG

>ENSMUST00000196745.4__Dclk1:269+402 134bp ATCAGTGCACTAGCGGTCG CTTGCTTATGGAACCGGTCG
ATCAGTGCACTAGCGGTCGcagcttccagacgctcgtgctccgcagcccc
agccgcgcccagcccggcgaggacagctccagcagccggccacagacaac
ccagcctccacccgCGACCGGTTCCATAAGCAAG


```

