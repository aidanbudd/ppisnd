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



