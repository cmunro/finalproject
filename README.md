# Final Project

## Introduction

This is a final project for the [Interacting with Data](https://github.com/Brown-BIOL2430-S04-Fall2015/syllabus) seminar in fall 2015. This project aims to visualize gene expression data, with an eye to showing specific Gene Ontology (GO) terms that relate to each differentially expressed gene (pairwise tissue comparisons, within a single species). GO terms were established as a consistent way to describe the biology of genes across different species, with very specific vocabulary to describe gene products that may be part of a 'Biological Process', be a 'Cellular Component', or have a specific 'Molecular Function' (each of these is a major GO domain). The GO ontology is structured in such a way that they have nested relationships, may have relationships with multiple terms in the same domain.

To view the project go to [this raw git page](https://rawgit.com/cmunro/finalproject/master/final_project.html).

## The data

These data are unpublished, and form a small part of my thesis work. I have pulled out raw counts for two major tissue types found in a siphonophore. I have computed genewise differences in the means between the two groups using EdgeR in R. I also mapped GO terms to the transcriptome using Blast2GO, and determined significantly enriched GO terms using the R package topGO.

The datafile included in this visualisation shows a very small fraction of total genes in the larger dataset. This is because I have only included genes that are present in these tissues, that also has a Blast hit and GO annotations. 

The data are organised in a tab delimited format, with log counts for two tissues on two columns. For each of the GO terms, I have calculated a mean gene expression value that is common to each of the genes that share these go terms. Here I have 4 GO terms, and 8 columns with updated gene expression values - this is either the same as before (if these genes don't have a particular GO value), or it has the same mean gene expression value. I also have two additional columns for each of the GO terms - one is the radius, which is sized relative to the number of genes that have a particular GO term; and the other is the colour, which changes from black to another colour depending on the GO term.

## Background

The goal of this project was to visualize gene expression patterns as a scatterplot, in a manner similar to [Casey's iris visualization](https://github.com/Brown-BIOL2430-S04-Fall2015/syllabus/tree/master/exercises/iris). I would like to be able to click on GO terms, and be able to visualise the relative number of genes that fall into this category, and provide a mean count for this group overall. Such a plot could be a starting point for a plot that would consider each of these GO terms in a more scientifically rigorous manner. 

## This project

### Mapping of data to aesthetics

Colour is used here to denote a different GO term. In this case, I have used red, yellow, green and blue for each of the GO term genes, and all other genes are black. Size is used to show how many genes are present for a particular GO term, so that I can map not only expression, but also the number of genes involved. I also used opacity for the "black" genes, to make it easier to determine how many genes are present, but I did not make the GO term genes opaque. This makes them easier to see against the black background.

### Filtering

All filtering took place before entering D3. This is only a subset of the overall genes, ones that have both a blast hit and associated GO terms.This is because the original dataset is far too large.

### Extra ink

I don't think there is any extra ink that does not map to the data. 

### Motion

Motion is used in this plot to show continuity between the raw counts and the average GO term genes. I intentially made the transition speed relatively slow, so that it is possible to see which genes are contributing to the average.

### Perspective

This is completely hard coded in advance, any exploration has been carried out in other programs like R, which I have also used to wrangle the data into a format that I can use in D3. This project serves more for exposition than exploration. 

## Assessment

This visualization did not provide an especially unique insight into my data. However, with the code in hand, I think it could be beneficial to include even more GO terms. At that point, there would be significantly fewer redundant graphs, and it would be relatively fast to switch between views of different GO terms.

Currently I feel that the main limitations of this approach are that the statistical possibilities are relatively limited. Any transformations that I would like to make to these data have to be done in advance, before passing it to D3.

Only looking at four GO terms is not enough - in the future, I'd like to see the top ten GO terms from all three domains here. 

