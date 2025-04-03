# Introduction 
beta-actin has been used in studies for cancer and inflammation. However, many studies use primer sets with only 1-4 mismatches against Lrrc58 (amplicon size ~ 154 bp), 
which may lead to off-target effects. 2 primer sets are being repeatedly used throughout the literature, both having some potential off-target effects as discussed. 
For example, in paper **Targeting the histone reader ZMYND8 inhibits antiandrogen-induced neuroendocrine tumor transdifferentiation of prostate cancer** 
[link](https://www.nature.com/articles/s43018-025-00928-z), they used this set: F:5'-GGCTGTATTCCCCTCCATCG-3'; R:5'-CCAGTTGGTAACAATGCCATGT-3'. Use this set as backup if the following design 
is not working.

# Primer Design Steps:
1. Usually I would select protein coding sequencing (consensus coding sequence, CCDS if possible). To find this:
   - Navigate to GenBank record of NM_007393.5, and then click "Graphics". You will be redirected to a view like below. Put your cursor on the protein sequence (NP_031419.1), and
     you can see that the protein is encoded by sequence starting 110-1237.
     - ![image](https://github.com/user-attachments/assets/fc3f0cc9-3788-4ef6-8d83-d0cd1b16d7ae)
2. Go to NCBI Primer Blast [link](https://www.ncbi.nlm.nih.gov/tools/primer-blast/). 
3. Primer Blast parameters (important ones below):
   - Enter NM_007393.5 as PCR template.
     - Forward primer from: 110
     - Reverse primer to: 1237
   - PCR product size: 80-200
   - Primer melting temperatures: 59-61 (max Tm difference = 1.5)
   - Exon junction span: Primers must span an exon-exon junction.
   - Specificity check: Enable search for primer pairs specific to the intended PCR template
   - Database: RefSeq mRNA
   - Exclusion: check "Exclude uncultured/environmental sample sequences"
   - Organism: "Mus musculus (taxid:10090)"
   - Advanced parameters:
     - Primer size: 16-24; Opt 20
     - Primer GC content: 30%-70%
4. Run the Primer Blast, we can select a primer set. This primer set spans an exon-exon junction in the coding sequence. Its potential unwanted products are either >1000 bp or having >= 4 mismatches on each forward/reverse primer.
   ```
       Primer pair 2
    	Sequence (5'->3')	Template strand	Length	Start	Stop	Tm	GC%	Self complementarity	Self 3' complementarity
    Forward primer	ATATCGCTGCGCTGGTCG	Plus	18	120	137	60.36	61.11	5.00	2.00
    Reverse primer	CCCACCATCACACCCTGG	Minus	18	246	229	59.64	66.67	3.00	3.00
    Product length	127
    Exon junction	232/233 (reverse primer) on template NM_007393.5
    Products on intended targets
    >NM_007393.5 Mus musculus actin, beta (Actb), mRNA
    
    
    product length = 127
    Forward primer  1    ATATCGCTGCGCTGGTCG  18
    Template        120  ..................  137
    
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        246  ..................  229
    
    Products on potentially unintended templates
    > XM_017313256.2 PREDICTED: Mus musculus ubiquitin-associated protein 1-like (Ubap1l), transcript variant X1, mRNA
    
    
    product length = 1821
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3856  T............T....  3839
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        2036  .......C.C..T....C  2053
    
    > XM_017316739.2 PREDICTED: Mus musculus LETM1 domain containing 1 (Letmd1), transcript variant X2, mRNA
    
    
    product length = 1067
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        6731  GAGC...G..........  6714
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        5665  ...C..CC..........  5682
    
    > XM_006521322.3 PREDICTED: Mus musculus LETM1 domain containing 1 (Letmd1), transcript variant X3, mRNA
    
    
    product length = 1067
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        6731  GAGC...G..........  6714
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        5665  ...C..CC..........  5682
    
    > XM_030248726.2 PREDICTED: Mus musculus LETM1 domain containing 1 (Letmd1), transcript variant X6, mRNA
    
    
    product length = 1067
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        6731  GAGC...G..........  6714
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        5665  ...C..CC..........  5682
    
    > XM_036159561.1 PREDICTED: Mus musculus LETM1 domain containing 1 (Letmd1), transcript variant X4, mRNA
    
    
    product length = 1067
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        6731  GAGC...G..........  6714
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        5665  ...C..CC..........  5682
    
    > XM_017314276.3 PREDICTED: Mus musculus glutamate receptor, ionotropic, NMDA2C (epsilon 3) (Grin2c), transcript variant X1, mRNA
    
    
    product length = 1826
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3802  A.TT......G.......  3785
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1977  ....G.TC.........C  1994
    
    > XM_017314277.3 PREDICTED: Mus musculus glutamate receptor, ionotropic, NMDA2C (epsilon 3) (Grin2c), transcript variant X2, mRNA
    
    
    product length = 1826
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3819  A.TT......G.......  3802
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1994  ....G.TC.........C  2011
    
    > XM_017314279.3 PREDICTED: Mus musculus glutamate receptor, ionotropic, NMDA2C (epsilon 3) (Grin2c), transcript variant X5, mRNA
    
    
    product length = 1826
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3802  A.TT......G.......  3785
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1977  ....G.TC.........C  1994
    
    > XM_011248738.4 PREDICTED: Mus musculus glutamate receptor, ionotropic, NMDA2C (epsilon 3) (Grin2c), transcript variant X4, mRNA
    
    
    product length = 1826
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3802  A.TT......G.......  3785
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1977  ....G.TC.........C  1994
    
    > XM_011248743.4 PREDICTED: Mus musculus glutamate receptor, ionotropic, NMDA2C (epsilon 3) (Grin2c), transcript variant X13, mRNA
    
    
    product length = 1826
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3802  A.TT......G.......  3785
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1977  ....G.TC.........C  1994
    
    > NM_001288625.1 Mus musculus AT-rich interaction domain 3A (Arid3a), transcript variant 2, mRNA
    
    
    product length = 72
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        345  GT.T........G....C  328
    
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        274  .......A.TGC......  291
    
    > NM_007880.4 Mus musculus AT-rich interaction domain 3A (Arid3a), transcript variant 1, mRNA
    
    
    product length = 72
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        499  GT.T........G....C  482
    
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        428  .......A.TGC......  445
    
    > XM_006513202.5 PREDICTED: Mus musculus AT-rich interaction domain 3A (Arid3a), transcript variant X2, mRNA
    
    
    product length = 72
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        456  GT.T........G....C  439
    
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        385  .......A.TGC......  402
    
    > XM_006513201.5 PREDICTED: Mus musculus AT-rich interaction domain 3A (Arid3a), transcript variant X1, mRNA
    
    
    product length = 72
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1294  GT.T........G....C  1277
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1223  .......A.TGC......  1240
    
    > NM_001288626.1 Mus musculus AT-rich interaction domain 3A (Arid3a), transcript variant 3, mRNA
    
    
    product length = 72
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        499  GT.T........G....C  482
    
    Reverse primer  1    CCCACCATCACACCCTGG  18
    Template        428  .......A.TGC......  445
    
    > XM_036156248.1 PREDICTED: Mus musculus matrix metallopeptidase 28 (epilysin) (Mmp28), transcript variant X1, mRNA
    
    
    product length = 1452
    Forward primer  1    ATATCGCTGCGCTGGTCG  18
    Template        196  .GC........A....G.  213
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1647  ..AT.TC..T........  1630
    
    > NM_009741.5 Mus musculus B cell leukemia/lymphoma 2 (Bcl2), transcript variant 1, mRNA
    
    
    product length = 2292
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        6077  AAG...T...........  6060
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3786  GG..TT...........T  3803
    
    > NM_019915.3 Mus musculus ADP-ribosyltransferase 2b (Art2b), mRNA
    
    
    product length = 1926
    Forward primer  1     ATATCGCTGCGCTGGTCG  18
    Template        1621  TG..T....A.......A  1638
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        3546  TT.TT.C...........  3529
    
    > XM_036154054.1 PREDICTED: Mus musculus tubulin, gamma complex component 3 (Tubgcp3), transcript variant X5, mRNA
    
    
    product length = 1502
    Forward primer  1    ATATCGCTGCGCTGGTCG  18
    Template        299  CCC.T...........A.  316
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        1800  TG.TG..C..........  1783
    
    > NM_198031.1 Mus musculus tubulin, gamma complex component 3 (Tubgcp3), mRNA
    
    
    product length = 1441
    Forward primer  1     ATATCGCTGCGCTGGTCG  18
    Template        1203  CCC.T...........A.  1220
    
    Reverse primer  1     CCCACCATCACACCCTGG  18
    Template        2643  TG.TG..C..........  2626
   ```
# Summary
Now we have the primer sequence for Actb:

Amplicon size 127bp
- Forward: 5'-ATATCGCTGCGCTGGTCG-3'
- Reverse: 5'-CCCACCATCACACCCTGG-3'
