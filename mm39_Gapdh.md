# Introduction
The primer design is from the paper **Reference genes for gene expression studies in the mouse heart**. [link](https://www.nature.com/articles/s41598-017-00043-9)

# Design
- Forward: 5'-CTCCCACTCTTCCACCTTCG-3'
- Reverse: 5'-GCCTCTCTTGCTCAGTGTCC-3'

# Validation using Primer Blast
In summary, this primer set will amplify a sequence crossing exon-exon junction with a length of 189bp. It amplifies all Refseq transcript variants of Gapdh. Some potential off-target amplicons 
may exist but there are many mismatches so will not matter that much.

```
Primer pair 1
	Sequence (5'->3')	Length	Tm	GC%	Self complementarity	Self 3' complementarity
Forward primer	CTCCCACTCTTCCACCTTCG	20	59.75	60.00	2.00	2.00
Reverse primer	GCCTCTCTTGCTCAGTGTCC	20	60.39	60.00	3.00	1.00
Products on target templates
>NM_001411845.1 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 8, mRNA


product length = 189
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1309  ....................  1328

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1497  ....................  1478

>NM_001411840.1 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 3, mRNA


product length = 189
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        891  ....................  910

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1079  ....................  1060

>NM_001289726.2 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 1, mRNA


product length = 189
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        973  ....................  992

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1161  ....................  1142

>NM_001411842.1 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 5, mRNA


product length = 189
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1107  ....................  1126

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1295  ....................  1276

>NM_001411844.1 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 7, mRNA


product length = 189
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1065  ....................  1084

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1253  ....................  1234

>NM_001411843.1 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 6, mRNA


product length = 189
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1007  ....................  1026

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1195  ....................  1176

>NM_008084.4 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 2, mRNA


product length = 189
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        933  ....................  952

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1121  ....................  1102

>NM_001411841.1 Mus musculus glyceraldehyde-3-phosphate dehydrogenase (Gapdh), transcript variant 4, mRNA


product length = 189
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1049  ....................  1068

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1237  ....................  1218

>NM_001360401.2 Mus musculus ER membrane associated RNA degradation (Ermard), transcript variant 4, mRNA


product length = 1484
Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2340  T.....A.A..........A  2321

Reverse primer  1    GCCTCTCTTGCTCAGTGTCC  20
Template        857  .TT.T..C..G.........  876

>NM_026605.3 Mus musculus symplekin (Sympk), transcript variant 1, mRNA


product length = 550
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1585  ....GG..T.A........T  1566

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1036  ..TG.A............G.  1055

>NM_001360713.2 Mus musculus symplekin (Sympk), transcript variant 2, mRNA


product length = 550
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1585  ....GG..T.A........T  1566

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1036  ..TG.A............G.  1055

>NM_001134300.3 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 2, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        2055  .......G.C.A.C.....C  2074

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2893  C.....G..TGG........  2874

>NM_001408243.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 13, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1692  .......G.C.A.C.....C  1711

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2530  C.....G..TGG........  2511

>NM_001408233.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 3, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1710  .......G.C.A.C.....C  1729

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2548  C.....G..TGG........  2529

>NM_001347235.1 Mus musculus spen family transcription repressor (Spen), transcript variant 2, mRNA


product length = 2531
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        5172  ....GG.......TG....T  5153

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2642  ..AG..GCA...........  2661

>NM_001408237.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 7, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1383  .......G.C.A.C.....C  1402

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2221  C.....G..TGG........  2202

>NM_019763.2 Mus musculus spen family transcription repressor (Spen), transcript variant 1, mRNA


product length = 2531
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        5241  ....GG.......TG....T  5222

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2711  ..AG..GCA...........  2730

>NM_001408240.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 10, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1365  .......G.C.A.C.....C  1384

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2203  C.....G..TGG........  2184

>NM_001408235.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 5, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        2037  .......G.C.A.C.....C  2056

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2875  C.....G..TGG........  2856

>NM_001408238.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 8, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1780  .......G.C.A.C.....C  1799

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2618  C.....G..TGG........  2599

>NM_001408242.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 12, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1457  .......G.C.A.C.....C  1476

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2295  C.....G..TGG........  2276

>NM_001408239.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 9, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        2125  .......G.C.A.C.....C  2144

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2963  C.....G..TGG........  2944

>NM_001001986.3 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 1, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1295  .......G.C.A.C.....C  1314

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2133  C.....G..TGG........  2114

>NM_001408234.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 4, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1475  .......G.C.A.C.....C  1494

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2313  C.....G..TGG........  2294

>NM_001408236.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 6, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        2355  .......G.C.A.C.....C  2374

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        3193  C.....G..TGG........  3174

>NM_001408241.1 Mus musculus nucleolar protein 4-like (Nol4l), transcript variant 11, mRNA


product length = 839
Forward primer  1     CTCCCACTCTTCCACCTTCG  20
Template        1277  .......G.C.A.C.....C  1296

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2115  C.....G..TGG........  2096

>NM_025911.2 Mus musculus coiled-coil domain containing 91 (Ccdc91), transcript variant 1, mRNA


product length = 508
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        504  A....T.......CA...G.  523

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1011  ..AGT..C.T..........  992

>NM_001355713.1 Mus musculus coiled-coil domain containing 91 (Ccdc91), transcript variant 2, mRNA


product length = 508
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        382  A....T.......CA...G.  401

Reverse primer  1    GCCTCTCTTGCTCAGTGTCC  20
Template        889  ..AGT..C.T..........  870

>NM_001355715.1 Mus musculus coiled-coil domain containing 91 (Ccdc91), transcript variant 4, mRNA


product length = 508
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        624  A....T.......CA...G.  643

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1131  ..AGT..C.T..........  1112

>NM_001355714.1 Mus musculus coiled-coil domain containing 91 (Ccdc91), transcript variant 3, mRNA


product length = 508
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        592  A....T.......CA...G.  611

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        1099  ..AGT..C.T..........  1080

>NM_144522.5 Mus musculus TBC1 domain family, member 10b (Tbc1d10b), mRNA


product length = 1839
Forward primer  1    CTCCCACTCTTCCACCTTCG  20
Template        512  .C.......GGA.......C  531

Reverse primer  1     GCCTCTCTTGCTCAGTGTCC  20
Template        2350  C.T..........CT.T...  2331
```
