---
title: Combined Cytoscape Session
layout: page
navigation: 62
author: Scooter Morris, Nadya Doncheva, Lars Juhl Jensen
---

### Network visualization of proteomics data

For this practical we will use data from the paper ["Temporal proteomics of NGF-TrkA signaling identifies an inhibitory role for the E3 ligase Cbl-b in neuroblastoma cell differentiation"](http://www.ncbi.nlm.nih.gov/pubmed/25921289). Specifically, we will use [Supplementary Table S3](Table_S3.xlsx).

If you have another suitable dataset yourself, you are of course welcome to use that instead.


### Obtaining a STRING network for a disease

Besides explicitly querying STRING for a list of proteins, the app also gives the option to obtain the list of proteins from other sources. One option to have it query the [DISEASES](http://diseases.jensenlab.org) for proteins associated with a disease of interest and fetch a STRING network for these.

- From "Import Network from Public Databases" select "STRING: disease query".
- Query for the disease of interest, e.g. "Alzheimer's", and select the correct disease term from the list.
- Specify the desired number of proteins for the disease and the STRING confidence cutoff.

This is all it takes to obtain a network for a disease. You can use the "Expand network" function of the app to add proteins, which are functionally associated with proteins linked to the disease (these might be new candidates). You may want to color the nodes in the network based on, for example, their tissue expression ("nervous system" would make sense for Alzheimer's disease) or target class ("pharos family").


### Obtaining a network of proteins associated with a PubMed query

The second way to have the app produce a protein list itself is to base it on a PubMed query. This works by first querying PubMed (via its REST interface) to obtain the list of PMIDs that match the query of interest. Next we search for proteins that are overrepresented in this list of PMIDs relative to PubMed as a whole. This is possible, because we have already before text mined the entire PubMed database; we thus know which abstracts mention which proteins. The list of the most overrepresented proteins then used to fetch a STRING network.

- From "Import Network from Public Databases" select "STRING: PubMed query".
- Choose the organizm of interest, e.g. "Arabidopsis thaliana".
- Enter the PubMed query, e.g. "arabidopsis stress response" (without quotes).
- Specify the desired number of proteins and the STRING confidence score.

When querying this way, it is always wise to first use the [PubMed web interface](http://www.ncbi.nlm.nih.gov/pubmed) to finetune the query. Once you are satisfied with the set of abstracts retrieved, simply copy the query into the app. Having retrieved the network, you can of course again use all of the Cytoscape functionality, for example, to color the nodes based on their subcellular compartment ("mitochondrion" would make sense for the example query).
