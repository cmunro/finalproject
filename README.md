# Final Project

## Introduction

This is a final project for the [Interacting with Data](https://github.com/Brown-BIOL2430-S04-Fall2015/syllabus) seminar in fall 2015. This project aims to visualize gene expression data, with an eye to showing specific Gene Ontology (GO) terms that relate to each differentially expressed gene (pairwise tissue comparisons, within a single species). GO terms were established as a consistent way to describe the biology of genes across different species, with very specific vocabulary to describe gene products that may be part of a 'Biological Process', be a 'Cellular Component', or have a specific 'Molecular Function' (each of these is a major GO domain). The GO ontology is structured in such a way that they have nested relationships, may have relationships with multiple terms in the same domain.

To view the project go to [https://rawgit.com/cmunro/finalproject/master/final_project.html](this raw git page).

## The data

These data are unpublished, and form a small part of my thesis work. I have pulled out raw counts for two major tissue types found in a siphonophore. I have computed genewise differences in the means between the two groups using EdgeR in R. I also mapped GO terms to the transcriptome using Blast2GO, and determined significantly enriched GO terms using the R package topGO.

The datafile included in this visualisation shows a very small fraction of total genes in the larger dataset. This is because I have only included genes that are present in these tissues, that also has a Blast hit and GO annotations. 


- Data structure - what are the variables? How are they organized? What states can they have

## Background

The goal of this project was to visualize gene expression patterns as a scatterplot, in a manner similar to [Casey's iris visualization](https://github.com/Brown-BIOL2430-S04-Fall2015/syllabus/tree/master/exercises/iris). I would like to be able to click on GO terms, and be able to visualise the relative number of genes that fall into this category, and provide a mean count for this group overall. Such a plot could be a starting point for a plot that would consider each of these GO terms in a more scientifically rigorous manner. 

## This project

### Mapping of data to aesthetics

How will aesthetic attributes ( X / Y / color / shape / size /texture / etc ) will be mapped to the data?

### Filtering

Are data filtered? ie in some views are some data not mapped to particular attributes of the image? What is the goal of the filtering?

### Extra ink

Are there aesthetic attributes that are not mapped to the data? If so, what purpose do they serve ( redundancy for robustness / improve visual metaphor / but data in context / beauty / etc )?

Are any data mapped to more than one aesthetic attribute? Why?

### Motion

Motion is used in this plot to show continuity between the raw counts and the average GO term genes. 

### Perspective

To what extent is perspective (eg mappings) controlled by users vs hard coded in advance? How does this project aid in exploration vs exposition?

## Assessment

Was the new visualization successful at providing insight that was not possible or more difficult with previous approaches?

What are the main limitations of new approach?

What are future directions this could go in?


