---
title: Short Linear Motifs
layout: page
author: Holger Dinkel
navigation: 53
---

# Objective: Get familiar with the [Phospho.ELM](http://phospho.elm.eu.org) resource.

**Presentation Slides**:

- [Short_Linear_Motifs.pdf](Short_Linear_Motifs.pdf)
- [Elm_Phospho_Switches.pdf](Elm_Phospho_Switches.pdf)

## Searching via protein id

1.  Go to [Phospho.ELM](http://phospho.elm.eu.org) and enter protein accession 'CASP9_HUMAN' in the second form field.
    1.  How many annotated sites/residues do you find? Which sites have information from multiple references? <!--- 8 out of 11 -->
    2.  How many are annotated as *high throughput experiments*? <!--- 4 -->
    3.  What information is given on the surface accessibility of the annotated residues?
    4.  (OPTIONAL) later during this course, when you've learned to use a 3D-viewer, use it to visualize the structure of ([1NW9](http://www.rcsb.org/pdb/explore/explore.do?structureId=1NW9)) and try to highlight the individual phosphorylatable residues and investigate their surface accessibility.

1.  Query Phospho.ELM for phosphorylation sites of protein '*Cyclin dependent kinase inhibitor 1B*' (use the accession P46527)
    1.  How many phosphorylation sites are annotated for this protein? <!--- 10 -->
    2.  Which sites are well conserved as well as reside in disordered region? (Tip: Click the column heads for sorting) <!--- Mod_CDK 187 -->
    3.  Are there any (MINT) interactions annotated for this protein? <!--- 7 -->
    4.  (OPTIONAL) Which of these interactions at MINT describe the phosphorylation reaction? <!--- 1 Akt1 -->

1.  Query Phospho.ELM for SRRM2_HUMAN to see a protein with a quite high number of phosphorylations. Can you estimate how many there are?
    1.  Have a look at how many of these annotations stem from low throughput experiments? (eg. **not** having 'HTP' as Source)

* * * * *

## Searching via gene name

Recently, you've learned about the protein 'EPSIN' and you are curious to know if there are any phosphorylation sites annotated for this protein.

1.  Go to [Phospho.ELM](http://phospho.elm.eu.org) and enter protein name 'epsin' in the *first* form field ('gene name').
    1.  You should see a table showing multiple hits in the database. Why? <!--- Multiple Epsins -->
    2.  Select 'Epsin 1'. Now you're at the results page. However, if you scroll down, you see results from multiple proteins. Why? <!--- Epsin-1 in Multiple Organisms -->
    3.  Which protein has the most annotation? <!--- Human -->
    4.  Go back to the Phospho.ELM startpage and query the database so that you'll receive only results for this one protein. <!--- Q9Y6I3 -->

2.  Start the Jalview Plugin and look at the conservation of the sequence (You're looking for high conservation in non-structured regions).
    1.  Can you spot any? <!--- Multiple DPWs, Watchout for conserved UIM region(s) -->

<!-- == Inspecting sequence conservation ==  -->
<!--  -->
<!-- \# Go to [UniProt](http://uniprot.org) and have a look at the sequence O14746 (TERT_HUMAN).  -->
<!-- \#\# How many isoforms of this sequence are known?  -->
<!-- \#\# What are the low throughput phosphorylation sites reported for the isoform 1? Compare the Uniprot data with the information for the same sequence in Phospho.ELM.  -->
<!-- \#\# Are the phosphosites equally conserved in the different isoforms?  -->
<!-- \#\# What can be the biological relevance of this conservation pattern? -->

* * * * *

## Using BLAST to find homologous information

1.  Search for Uniprot id 'ABL1_MOUSE'
    1.  How many annotated phosphorylation sites do you find? <!--- three -->

2.  Next, run [PhosphoBlast](http://phospho.elm.eu.org/pELMBlastSearch.html) on the [sequence](file:sequences_ELM.fasta) or ID of 'ABL1_MOUSE'.
    1.  How many phosphorylation sites are found? <!--- 30 -->
    2.  Why the difference? <!--- BLAST=Search in homologous sequences -->
    3.  In which proteins / organisms? <!--- Abl, Abl2, TRKB / Human, mouse, Caenorhabditis, Drosophila -->

<!-- * * * * * -->
<!--  -->
<!-- ## Comparing predictions from multiple sources: -->
<!--  -->
<!-- 1.  Go back to the phospho.elm startpage and search for uniprot id 'EGFR_HUMAN'. -->
<!--     1.  Use the link to go to Uniprot, scroll down (or click on 'Sequence annotation') and try to get an idea of the protein topology in order to be able to answer the next question. --> <!--- -645 = extracellular -->
<!--     2.  In which part of the protein do the most phosphorylations seem to be located? --> <!--- Carboxy-Terminus \> 678 -->
<!--     3.  (OPTIONAL) There are quite a lot of annotations, several of which come from high-throughput sources which generally are of lower quality. Go back to the search form, tick the box 'Do not show high throughput data' and rerun the search again. You should see significantly fewer results. -->
<!--     4.  (OPTIONAL) Use [IUPred](http://iupred.enzim.hu) to predict the disorder content of EGFR_HUMAN. Discuss these findings with your neighbor. -->
<!--  -->
<!-- 1.  Submit the [sequence](http://uniprot.org/uniprot/P49023.fasta) of Paxillin (P49023) to [DisPhos](http://www.dabi.temple.edu/disphos/) (default parameters) and [NetPhos](http://www.cbs.dtu.dk/services/NetPhos) -->
<!--     1.  Run [Iupred](http://iupred.enzim.hu) (make sure to generate an output plot) on the sequence to get an idea of the likely globular/disorder composition of the protein. -->
<!--     2.  Compare the results between NetPhos and DisPhos in particular with respect to phosphorylation sites in the carboxy terminus. -->
<!--     3.  Rerun the analysis of Paxillin (P49023) at [DisPhos](http://www.dabi.temple.edu/disphos/), this time instead of 'Default Predictor' select 'H. sapiens' as __organism__ -->

<!-- \# Search [Phospho.ELM](http://phospho.elm.eu.org) for P46844 (BIEA_RAT) -->
<!-- \#\# How many phosphorylation sites are annotated for this protein? -->
<!-- \# Try to run [DisPhos](http://www.dabi.temple.edu/disphos/) on the [sequence](http://uniprot.org/uniprot/P46844.fasta) of this protein (P46844). -->
<!-- \# Next, submit the sequence to [PhosphoBlast](http://phospho.elm.eu.org/pELMBlastSearch.html) -->
<!-- \#\# How many phosphorylations sites in homologous proteins do get? -->
<!-- \#\# In which / how many proteins? -->
<!-- \#\# Compare the findings of PhosphoBlast with the predictions of DisPhos -->
<!-- \#\# (OPTIONAL) later during this course, when you've learned to use a 3D-viewer, use it to visualize the structure of ([2H63](http://www.rcsb.org/pdb/explore/explore.do?structureId=2h63)) and try to highlight the individual phosphorylatable residues and investigate their surface accessibility.-->


<!-- \# Search Phospho.ELM for gene name KLF4 -->
<!-- \#\# How many phosphorylation sites are annotated for this protein? -->

<!-- \#\# Can you retrieve more information by using Phospho.Blast? -->

<!-- \# Retrieve information about phosphorylation of protein SRC_HUMAN (accession P12931) -->
<!-- \# How many phosphorylation sites are annotated for this protein? -->
<!-- \# Limit this information to residue 530 (of the same protein) -->

<!--(see chapter : *REST queries*) -->
<!-- \# (OPTIONAL) Try to get the same information in CSV (comma separated values) format -->
<!-- (see <http://phospho.elm.eu.org/help.html>) -->
<!-- \# Start JalView to see the conservation of phosphorylation sites -->



<!-- Phosphorylation of S62 in the SH3-binding motif of Myc proto-oncogene protein (MYC) by GSK-3 subfamily disrupts its interaction with Myc box-dependent-interacting protein 1 (BIN1). -->
<!-- <http://switches.elm.eu.org/switch.php?switch=SWTI000182> -->

<!-- Phosphorylation of LIG_SH2_SRC in DAB1 mediates binding to SRC -->
<!-- <http://switches.elm.eu.org/switch.php?switch=SWTI000623> -->

<!-- \#\#\#PTN3_HUMAN\#\#\# -->
<!-- Lots of features, annotated elms in structural region, phospho-dependant motif (14-3-3) -->

<!-- \#\#\#AMPH_HUMAN\#\#\# -->
<!-- False Positive -->

<!-- \#\#\#TNR11_MOUSE\#\#\# -->
<!-- TP\#FP -->


<!---% Maybe: -->
<!-- IGF1-R (Receptor tyrosine kinase) -->
<!-- Seq-ID: P08069 [Homo sapiens] -->

<!-- ZAP70_HUMAN -->

<!-- P18608|HMGN1_MOUSE -->

<!-- Compare the annotations with the prediction results from DisPHos -->

<!-- [DisPhos](http://www.dabi.temple.edu/disphos/) -->

<!-- Compare with Phospho.BLAST results -->

<!-- Maybe: P36507 -->

* * * * * 

# PhosphoSitePlus:

Get familiar with PhosphoSitePlus:

This resource has an enormous collection of PTMs, referenced to the source literature. It has a symbiotic relationship with Cell Signaling Technology and links to their antibodies.

The interface is a bit confusing at first glance so the exercises will show you to find information.

1. Open [PhosphoSitePlus](http://www.phosphosite.org/) and search for p53 using the available search window
    1. How many proteins are retrieved?
    1. What are the modifications found in p53? (Mouse over show legend)
    3. Click on the links to find out what you get.
    4. Use that experience to click on the human p53 page. 
        - Find the graphic with modifications. 
        - Are PTMs mostly in the ~100AA disordered termini or in the folded DNA-binding domain?
    5. Some PTMs sites can't be clicked on in the graphic. 
        - Why might that be? To find out, track down where the PTM evidence comes from for the Cysteine residue C229.
    6. Examine the large table of PTMs from different organisms. 
        - What is LTP and what is HTP? 
        - Which evidence type is more reliable? 
        - Is it good to have both? 
        - Is the residue with the most evidence important for function?
    7. How many p53 sites are sumoylated? 
        - Is there any overlap of sumoylation and other PTMs?
    8. Click to get the multiple alignment. 
        - Does mouse p53 have more experimental sites than human?

1. (OPTIONAL) We would like to find proteins which are phosphorylated by the CSK kinase. For this we use the pattern from the ELM class [MOD_TYR_CSK](http://elm.eu.org/elms/MOD_TYR_CSK). Go back to the [PhosphoSitePlus](http://www.phosphosite.org/) home page and click on ‘Protein, Sequence or Reference search’
    1. In the motif search box type in the reg-exp for [MOD_TYR_CSK](http://elm.eu.org/elms/MOD_TYR_CSK) like this: ``[TAD][EA]xQY[QE]x[GQA][PEDLS]``
    1. Click search
    1. The result page will give you the list of the protein matches
    1. Use the links to the human JMJD3 and BPAG1 proteins to try to find out which of these are likely to actually be phosphorylated by CSK. Have a look at the number of LTP vs. HTP references. Also follow the link to STRING to see if there are any interactions with CSK annotated.

* * * * *

# Objective: Get familiar with ELM 

[ELM](http://elm.eu.org)  (Eukaryotic Linear Motif)
__prediction tool__.

<!--- <file:ELM_Eukaryotic_Linear_Motif_Resource.DinkelHolger.pdf> -->

1.  Search protein SRC_HUMAN (accession P12931) for ELMs using the following parameters:
    -   Cell Compartment: **Not specified**
    -   Motif Probability Cutoff: **100**
    -   Taxonomic Context: (leave blank)
    1.  How many instances do you find?
<!---% \#\# How many elm classes (not instances) have been completely filtered (all their instances have been filtered)? -->
    1.  Redo the search (again accession P12931) now using these parameters:
    -   Cell Compartment: **cytosol**
    -   Motif Probability Cutoff: **0.01**
    -   Taxonomic Context: Homo sapiens
    1.  How many instances do you find now?
<!--- \#\# How many elm classes (not instances) have been completely filtered (all their instances have been filtered)? -->
    1.  How many of the instances are 'annotated'?
    2.  Do the structural predictors/filters (SMART, GlobPlot, IUPRED, Secondary Structure) agree in terms of which regions are structured/disordered?
    3.  Compare the location of the annotated instances with structural information at hand (IUPRED, Secondary Structure).
    4.  For the annotated instances, which of the ELM classes __require__ a phosphorylation at a certain residue of the motif? (Hint: This information can be found in the description of the ELM class)
    5.  Which residue in SRC_HUMAN corresponds to this and can you find evidence for a phosphorylation of this residue (using Phospho.ELM)?
<!--- % \# Earlier today you searched Phospho.ELM for CDN1B_HUMAN and investigated the most conserved phosphorylation site. Try to find this using ELM % -->
<!--- 1.  Earlier today you searched Phospho.ELM for 'Epsin1' and investigated the most conserved phosphorylation site. Try to find these using ELM. -->
<!---    1.  Start the Jalview plugin to visualize the conservation of motifs in 'Epsin1'. -->

1.  Submit the following [sequence](http://uniprot.org/uniprot/P49023.fasta) to ELM, using default parameters, no cellular compartment.
    1.  Compare the results with a search for the same sequence when using the __cellular compartment__ 'plasma membrane'
    2.  Are there any phosphorylations annotated for the carboxy terminus of this protein? Why?

2.  There are three annotated instances of the ELM class LIG_NRBOX in the protein NCOA2_HUMAN. Do they reside in ordered or disordered regions (according to IUPred and SMART)?

1.  Search ELM for the following proteins and familiarize yourself with the different modular organizations of the following proteins. You should focus on the different types of protein architectures, the different amount of information which is available from different resources as well as where functional motifs are located / in which part of the protein would you expect them? Feel free to click on the link to resources such as 'Uniprot' or 'SMART', to get more information about the selected protein.
    1.  EGFR_HUMAN
    2.  CASP9_HUMAN
    3.  EPN1_HUMAN
    4.  SMAD3_HUMAN <!--- Phosphorylation sites = Docking sites -->
    5.  SOS1_HUMAN
    6.  PTN3_HUMAN
    7.  SRRM2_HUMAN
    8.  KMT2D_HUMAN
    9.  KI67_HUMAN <!--- disorder, many phosphorylation sites -->
    10. AP180_HUMAN
    11. Q94833_TRIVA
    12. AMPH_HUMAN
    13. MAPK2_HUMAN
    14. CTNB1_HUMAN
    15. JUN_HUMAN <!--- lot of annotated instances -->


<!---% \# Search elm.eu.org using the protein name 'CASP9_HUMAN' and look for the % -->

1.  Search elm.eu.org using the protein name 'MDM4_HUMAN' and look for the 'USP binding motif' DOC_USP7_1.
    1.  How many such motif instances are found in this protein sequence? <!--- 6 -->
    2.  Try to assess the biological relevance of each of these instances. <!--- 2 TP, 2 TN, 2 Unknown -->
    2.  (OPTIONAL) Repeat this exercise with protein 'AMPH_HUMAN' and ELM class 'LIG_Clathr_ClatBox_1'
    1.  (OPTIONAL) Is the annotation for the biological relevance in accordance with the globular structure?

1.  You're studying the cell surface expression of a receptor and find out that some isoforms are expressed at the surface (Q05586-2) while another isoform is retained in the endoplasmatic reticulum (Q05586-5). You want to investigate a possible role of linear motifs in this phenomenon.
    1.  First, align these sequences to see which parts are similar/identical and which are different (go to <http://www.uniprot.org/uniprot/Q05586>, scroll down to 'sequences', select isoforms 2 and 5 and click 'align').
    2.  Then use <http://elm.eu.org> to scan these sequences for linear motifs, using cell compartment filter 'cytosol'. You're looking for targeting motifs (TRG\_\*).
    3.  By looking through the annotations of these targeting ELM classes, can you find motif instances that might be responsible for the different behaviour of the isoforms?
    4.  If there are multiple instances of that motif found per protein, can you use differential information (comparing the motifs found in the different isoforms) to narrow down the number of candidate instances?
    5.  Next, you sequence another isoform (Q05586-4) which also features this motif at a homologous position, but strangely does not get expressed at the cell surface. You discuss this with your colleague and he tells you that he recently found out that this protein also binds to the PDZ domain of DLG4. Can you come up with a hypothesis how this all fits together?
1.  (OPTIONAL) Search for linear motifs in the protein sequence SMAD3_HUMAN.
    1.  (OPTIONAL) Which annotated instances can you see?
    2.  (OPTIONAL) Click on one of the annotated docking motifs to read about a switching mechanism involving these motifs. How does this switch work?

<!--- @switches <http://switches.elm.eu.org/switch.php?switch=SWTI000279> CDK8/9 phosphorylates Mothers against decapentaplegic homolog 3 (SMAD3) at T179 and S208. -->
<!-- Phosphorylation of T179 creates a binding site for the WW domain of Peptidyl-prolyl cis-trans isomerase NIMA-interacting 1 (PIN1), while phosphorylation of S20 -->

<!-- == Conservation == -->
<!-- Go to UniProt and get the fasta sequences of: AMPH_HUMAN and BIN1_HUMAN, two members of the BAR adaptor protein family. Use each sequence as input for the Conscore. -->

<!-- Start the two Jalview interfaces and focus on the multiple sequence alignments: why are the sets of homologous sequences not equal? -->
<!-- Have a look at the list of top ranked instances (CS = 1.0) and make a quick assessment of the main differences in terms of conserved ELM classes. Remember to consider only the instances located outside the BAR and SH3 domains (positions 270 to 500 in BIN1_HUMAN and 240 to 600 in AMPH_HUMAN). Are such discrepancies bigger/smaller than expected given the dissimilar alignments? Why? -->

<!-- - Use the curated alignment of the BAR adaptor protein family as input for the Conscore taking AMPH_HUMAN as the leading sequence (do not close this result page, we will be using it again for exercise 4). -->

<!-- Observe the output. Describe the scenarios where the multiple sequence alignment input should be preferred. -->

<!--- CASP9_HUMAN cleavage site? -->

1.  (OPTIONAL) Caspase 9 is mainly globular protein. Focus on the carboxyterminal globular domain (CASc Caspase, interleukin-1 beta converting enzyme) and try to assess which modification sites (MOD\_) are surface accessible (Hint: Mouse-over to find high accessibility scores with low p-values)


* * * * *

# Objective: Get familiar with the ELM database
the [ELM (Eukaryotic Linear Motif)](http://elm.eu.org) __database__.

## Instances


1.  (OPTIONAL) Search protein UNG_HUMAN (P13051) for ELMs.
    1.  For the annotated instances, which of these ELM classes require a phosphorylation at a certain residue of the motif? (Hint: This information can be found in the description of the ELM class)
    2.  Which amino acid residue in UNG_HUMAN corresponds to this and can you find evidence for a phosphorylation of this residue (using Phospho.ELM)? <!--- 60 & 63 -->

1.  (OPTIONAL) Get all annotated instances that contain the search term "retinoblastoma" (again, using url <http://elm.eu.org/elms/browse_instances.html>)
    1.  Compare the number of human instances with the number of viral instances.
    2.  Read the abstract for the ELM class LIG_Rb_LxCxE_1 to find out why so many viral proteins interact with Rb.

1.  (OPTIONAL) Search [Pubmed](http://www.ncbi.nlm.nih.gov/pubmed) for the terms "noonan syndrome" AND “motif” (you should get exactly one resulting publication, if not, make sure you use quotes around '"noonan syndrome"')
    1.  find the protein sequence that was analysed in this publication, retrieve the sequence from uniprot and submit it to ELM. Can you find the two mutation hotspots that are responsible for the syndrome described in the publication?

1.  (OPTIONAL) Get all annotated instances for *Homo sapiens* that contain the search term *ciliar* (Hint: Use [http://elm.eu.org/elms/browse_instances.html](http://elm.eu.org/elms/browse_instances.html))
    1.  How many are there?
    2.  Which experimental evidence is annotated and how reliable is this evidence?
    3.  Try to get these instances as TSV-file (tab separated values)

## Pathways


1.  (OPTIONAL) Go to the ELM Pathways page (ELM db -> ELM Pathways) and type "jak" into the search field.
    1. From the search results, click on the link "Jak STAT signaling pathway" for the human pathway (hsa04630)
    1. In the KEGG pathway map, try to locate the "SOS" protein.
    1. Which color is it? (You might need to go back to the ELM pathway page to see the color legend) What does that mean?
    1. Go back tho the ELM database and search for annotated instances in the SOS1_HUMAN protein (use the quick search at the top right of the
       ELM page)
    1. Click on the instance with startposition 1151. Which interaction has been annotated for this instance? Do you find this interactor in the
       KEGG pathway? Which domain(s) does this protein consist of? Which motif in SOS1_HUMAN does it interact with?

* * * * *

<!---  -->
<!-- == Interactions ==  -->
<!-- BIN1_HUMAN  -->

# switches.elm.eu.org:

1. Search [Phospho.ELM](http://phospho.elm.eu.org) for transcription factor 'Fos' (id P01101).
1. You would like to find out which of these annotated phosphorylation sites are involved in switching mechanisms annotated at [Switches.ELM](http://switches.elm.eu.org)? 
    1. For this, enter ``P01101`` into the switches.elm search box ``Search database`` and click submit.
    1. How many switching motifs do you find?
    1. What type are these?
    1. Click on the first one and investigate the role of the phosphorylation.

1. (OPTIONAL) Use the "Analyse" function at switches.elm and submit the accession number ``O70601``.
    1. Select residues 170-180 and click submit.
    1. Using the visualization to the right and focussing on the area highlighted by the ``Motif of interest``, what can you find out about:
        1. modified residues?
        1. region of interest?
        1. possible motifs mediating an interaction?

# ProViz:

1. Search [ProViz](http://proviz.ucd.ie) for 'Epsin1', find the human Epsin1 protein and click on 'view'.
    1. get an overview of this protein's architecture by clicking on the "condensed view" ("star" symbol) in the top right
    1. Try to locate the DPW motifs that you investigated in Jalview (First try to find them by eye, investigating sequence conservation in the alignment, then use the "search" function)
1. Search [ProViz](http://proviz.ucd.ie) for 'CDKN1B', find the human protein and click on 'view'
    1. Try to find a [Cyclin](http://elm.eu.org/elms/DOC_CYCLIN_1.html) interaction motif (you can use a regular expression from ELM if you want to).
    1. Does it reside in a structured or unstructered region of the protein?
    1. Can you find information about a switching mechanism that this motif is involved in?


# References:
1. Dinkel H, Van Roey K, Michael S, Kumar M, Uyar B, Altenberg B, Milchevskaya V, Schneider M, Kühn H, Behrendt A, Dahl SL, Damerell V, Diebel S, Kalman S, Klein S, Knudsen AC, Mäder C, Merrill S, Staudt A, Thiel V, Welti L, Davey NE, Diella F, Gibson TJ. (2016) "**ELM 2016-data update and new functionality of the eukaryotic linear motif resource.**" Nucleic Acids Res 44 [[URL](http://europepmc.org/abstract/MED/26615199)]
1. Gibson TJ, Dinkel H, Van Roey K, Diella F. (2015) "**Experimental detection of short regulatory motifs in eukaryotic proteins: tips for good practice as well as for bad.**" Cell Commun. Signal 13(1) [[URL](http://europepmc.org/abstract/MED/26581338)]
1. Van Roey K, Uyar B, Weatheritt RJ, Dinkel H, Seiler M, Budd A, Gibson TJ, Davey NE. (2014) "**Short Linear Motifs: Ubiquitous and Functionally Diverse Protein Interaction Modules Directing Cell Regulation**" Chem Rev. 2014 Jun 13.  [[URL]([http://pubs.acs.org/doi/abs/10.1021/cr400585q])]
1. Davey NE, Van Roey K, Weatheritt RJ, Toedt G, Uyar B, Altenberg B, Budd A, Diella F, Dinkel H and Gibson TJ (2012), **"Attributes of short linear motifs"**, Mol Biosyst., Jan, 2012. Vol. 8, pp. 268-281. [[DOI]([http://dx.doi.org/10.1039/c1mb05231d)] [[URL]([http://dx.doi.org/10.1039/c1mb05231d)] 
1. Davey NE, Travé G and Gibson TJ (2011), **"How viruses hijack cell regulation"**, Trends Biochem Sci., Mar, 2011. Vol. 36, pp. 159-169. [[DOI](http://dx.doi.org/10.1016/j.tibs.2010.10.002)] [[URL]([http://dx.doi.org/10.1016/j.tibs.2010.10.002)] 
1. Dinkel H, Chica C, Via A, Gould CM, Jensen LJ, Gibson TJ and Diella F (2011), **"Phospho.ELM: a database of phosphorylation sites--update 2011."**, Nucleic Acids Res., Jan, 2011. Vol. 39(Database issue), pp. D261-D267. [<span style="line-height: 1.5;">[[DOI](http://dx.doi.org/10.1093/nar/gkq1104)<span style="line-height: 1.5;">] [<span style="line-height: 1.5;">[[URL](http://dx.doi.org/10.1093/nar/gkq1104)<span style="line-height: 1.5;">] 

see also:

1. Jehl P, Manguy J, Shields DC, Higgins DG, Davey NE. "**ProViz-a web-based visualization tool to investigate the functional and evolutionary features of protein sequences.**" Nucleic Acids Res. 2016 Apr 16. [[URL](http://nar.oxfordjournals.org/cgi/pmidlookup?view=long&pmid=27085803)]
1. Dyson HJ and Wright PE (2005), **"Intrinsically unstructured proteins and their functions"**, Nat Rev Mol Cell Biol., Mar, 2005. Vol. 6, pp. 197-208. [[DOI]([http://dx.doi.org/10.1038/nrm1589)] [[URL]([http://dx.doi.org/10.1038/nrm1589)] 

* * * * *
