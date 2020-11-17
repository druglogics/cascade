# CASCADE - CAncer Signaling CAusality DatabasE

<!-- badges: start -->
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4066665.svg)](https://doi.org/10.5281/zenodo.4066665)
<!-- badges: end -->

This repository contains **manually curated causal interactions** to describe cancer signaling events and is compliant with the annotation standard established by the [SIGNOR database](http://signor.uniroma2.it/).

## Versions

There are different versions of the CASCADE topology:

1. **CASCADE 1.0** (75 nodes, 149 directed interactions).
GINsim files are available at the respective [GINsim model repository](http://ginsim.org/node/194).
This version was featured in Flobak et al. (2015). Discovery of Drug Synergies in Gastric Cancer Cells Predicted by Logical Modeling. *PLOS Computational Biology*, 11(8), e1004426. https://doi.org/10.1371/journal.pcbi.1004426

    Note that a slight different version of this topology (mostly node renaming, with a total of 77 nodes and 149 interactions) was used as a base file to build the later versions - see [cascade_1.0.sif](https://github.com/druglogics/cascade/blob/master/cascade_1.0.sif).

2. **CASCADE 2.0** (144 nodes and 367 interactions - see [cascade_2.0.tsv](https://github.com/druglogics/cascade/blob/master/cascade_2.0.tsv) and [cascade_2.0.sif](https://github.com/druglogics/cascade/blob/master/cascade_2.0.sif)).
This version was featured in Niederdorfer et al. (2020). Strategies to Enhance Logic Modeling-Based Cell Line-Specific Drug Synergy Prediction. *Frontiers in Physiology*, 11, 862. https://doi.org/10.3389/fphys.2020.00862
3. **CASCADE 3.0** (183 nodes and 603 interactions - see [respective directory](https://github.com/druglogics/cascade/tree/master/CASCADE_3.0) with files).
This version was featured in Tsirvouli et al. (2020). A middle-out modeling strategy to extend a colon cancer logical model improves drug synergy predictions in epithelial-derived cancer cell lines. *Frontiers in Molecular Biosciences*, 7, 300. https://doi.org/10.3389/fmolb.2020.502573

## Pathways

The database contains a series of molecular causality statements where influence of upstream signaling entities (e.g proteins) to downstream signaling entities (e.g. proteins) is explicitly given, in a signed and directed manner.
The CASCADE topology was built from a node-centric view and version 2.0 covers the following pathways:

- PI3K/AKT signaling pathway
- MAPK-signaling pathways (JNK, MAPK14, ERK)
- TGFBR-signaling pathway
- JAK-STAT signaling pathway
- WNT-CTNNB1 signaling pathway
- NFkB signaling pathway

These pathways are linked to prosurvival and antisurvival cell signaling (e.g. cyclin expression and caspase activation).

## Convert from Signor to SIF

The [cascade_to_sif.Rmd](https://github.com/druglogics/cascade/blob/master/cascade_to_sif.Rmd) R code can be used to convert the SIGNOR data (`.tsv`) to a topology (`.sif`) file.
The example in the code re-creates the `cascade_2.0.sif` (CASCADE 2.0 version).

## Citation Info

Eirini Tsirvouli, Barbara Niederdorfer, John Zobolas, Touré Vasundra, Åsmund Flobak, & Martin Kuiper. (2020, October 5). CASCADE - CAncer Signaling CAusality DatabasE (Version 3.0). Zenodo. http://doi.org/10.5281/zenodo.4066665

## Contact

- CASCADE 1.0: [asmund.flobak@ntnu.no](asmund.flobak@ntnu.no)
- CASCADE 2.0: [barbara.niederdorfer@ntnu.no](barbara.niederdorfer@ntnu.no)
- CASCADE 3.0: [eirini.tsirvouli@ntnu.no](eirini.tsirvouli@ntnu.no)
