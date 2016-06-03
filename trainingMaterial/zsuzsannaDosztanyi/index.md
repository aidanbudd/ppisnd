---
title: Intrinsically disordered proteins
layout: page
navigation: 52
author: Zsuzsanna Dosztanyi
---


---
title: Prediction of protein disorder
author: Zsuzsanna Dosztanyi
---

# Tutorial

## Exercise 1

### DISPROT database and analyzing calcineurin A

1.  Find calcineurin A (PP2BA\_HUMAN) in DISPROT
    [www.disprot.org](http://www.disprot.org/)
    
    (DP00092)

    You can start from UNIPROT, it has a link to DISPROT 
    or search DISPROT directly by keyword (sequence search does not work).

    1. What kind of information can you find on this page?
    2. Which regions are marked as disordered in DISPROT?
    3. Which regions are marked as ordered DISPROT?
    4. By what experimental techniques?
    5. What is the role of the disordered segments?




##  Exercise 2 

### Disorder prediction methods 

1.  Collect prediction outputs for calcineurin A using various methods!


The input can be (depending on the method):

- the amino acid sequence in FASTA format
- amino acid sequence in raw format (without header)
- UNIPROT ID or accession number

Please note

* some methods are sensitive to line breaks.
* In some cases the header cannot be too long or more then one word
* There could be restrictions on minimum and maximum length of sequence 

Some disorder prediction methods:

- IUPred [http://iupred.enzim.hu](http://iupred.enzim.hu/)
- Globplot [http://globplot.embl.de/](http://globplot.embl.de/)
- PONDR-FIT
[http://www.disprot.org/pondr-fit.php](http://www.disprot.org/pondr-fit.php)
- ESpritz
[http://protein.bio.unipd.it/espritz/](http://protein.bio.unipd.it/espritz/)
- PredictProtein
[http://ppopen.informatik.tu-muenchen.de/](http://ppopen.informatik.tu-muenchen.de/)
(MD, UCON, Norsp, Profbval)
- DISOPRED3 [http://bioinf.cs.ucl.ac.uk/psipred/](http://bioinf.cs.ucl.ac.uk/psipred/)
      (choose Disopred2 and 3 option!!!)
- or any other method you like...


2. Do the predictions agree with the experimental characterization of disorder?
3. Do the predictions agree with each other?
4. Which method predicts the most disorder?
5. Note the differences in the running time of the methods.



## Exercise 3 

### MobiDB database

1. Find calcineurin in MOBIDB
 [http://mobidb.bio.unipd.it/entries/Q08209](http://mobidb.bio.unipd.it/entries/Q08209)

You can find the output of several other methods there.

1. Which regions are predicted as disordered by the majority of methods?
2. Which regions have matching PDB structure?
3. Can you find regions that cannot be unambigiously assigned? 
    What could be the reason for that?    



## Exercise 4

### Analyze the protein with the Uniprot acession: P05204
Find the corresponding Disprot entry (DP00039 )
   
1. Predict protein disorder for DISPROT DP00039, for example with IUPred
2. Count number of positively charged amino acids
3. Count number of negatively charged amino acids
4.  Calculate net charge 
    (you can use the [protparam](http://web.expasy.org/protparam/) server)
5. Check low complexity segments 
    - log on to the server machine using either putty (on WIndows) or your terninal (linux or Mac)
    - download the sequence using the following command:
     
    wget http://www.uniprot.org/uniprot/P05204.fasta
     
     This command downloads the sequence to your current directory
    - run seg command on your sequence, this will indicate low complexity regions in your sequence  in lower case letters
   
    seg P05204.fasta

	(or you can take these from PFAM through  uniprot)

6. Check PFAM domains

Is there a contradiction between PFAM domain assignments and predicted disorder?



## Excercise 6

### Characterize human N-WASP ([O00401](http://www.uniprot.org/uniprot/O00401)) protein from the viewpoint of order and disorder

1. You can check PDB structures for this protein here:
    [http://www.rcsb.org/pdb/protein/O00401](http://www.rcsb.org/pdb/protein/O00401)
2. Find PFAM families and  check their type

    1. Click on the domain
    2. Click on "Curation and model"
    3. Check type: 

       - domain 
       - family
       - motif

3. Find low complexity regions (you can use pfam annotations). Which amino acids dominate in the low complexity region?
4. Predict disorder (e.g. with IUPred)
5. Which regions would you call disordered?


Now find binding regions located within disordered segments

1. Using the accession number for human N-WASP, find the data for this protein in the IDEAL database
IDEAL [http://www.ideal.force.cs.is.nagoya-u.ac.jp/IDEAL/](http://www.ideal.force.cs.is.nagoya-u.ac.jp/IDEAL/)
2. Can you find regions for this proteins that are annotated as disordered binding regions (called **ProS** in this database) ?
3. Predict disordered binding regions using ANCHOR [http://anchor.enzim.hu](http://anchor.enzim.hu/) 
or [MORF_chibi]()


## Exercise 7

###   Filtering motif hits

Dynein light chain protein binds to disordered segments that have a TQT binding motifs. One of its known interaction partner is FA83D ( Q9H4H8 ) with the region `VGTQTS`.
We found  the same sequence fragment in the protein `ASNSD1`.

 
1. Do you think it can be a valid binding partner?

Hint: Predict disordered binding regions (e.g. with ANCHOR)

You can add the `VGTQTS` motif to the search too in the motif window

Is the matching region predicted to have a disordered binding region?










