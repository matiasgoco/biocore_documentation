---
title: Introduction to NCBI
author: "Nathaniel Maki"
date: "May 17th, 2020"
---
# Introduction to NCBI

## Learning Objectives
* Acquire a basic understanding of the NCBI website, its resources, and its most commonly used utilities/tools
* More specifically, become familier with Pubmed, the Gene Expression Omnibus (GEO), BLAST, and briefly the Sequence Read Archive (SRA)
* Exposure to future and upcoming tools/resources under active development, such as NCBI Datasets, NCBI Virus Repository, and BLAST+

## What is NCBI?
* National Center for Biotechnology Information
* Three main focuses:
* Maintain a vast repository of data, generated by researchers from all over the world
  * Reflected through databases such as GEO, SRA, etc
* Develop tools, utilities, and software for procuring available data, and for performing analysis
  * BLAST, SRA-toolkit, RAPT
* Provide a web interface for interacting with, manipulating, and querying said data

In addition the the above, they also produce training materials to assist in orienting students, fledgling researchers, and seasoned PIs to the tools/resources they offer. 

The following [Link](https://www.ncbi.nlm.nih.gov/home/learn/) will take you to the NCBI education page.

## Platform overview
<img src="./ncbi_images/ncbi_home.png" width="800">

The front page of NCBI acts as a hub of sorts, with the main source of navigation being the search bar, and dropdown menu beside it. At the top left of the page are quick links to resources available, as well as grouped tutorials covering common use cases.

<img src="./ncbi_images/ncbi_resources_dropdown.png" width="400">

Selecting BLAST will take you to the tools' homepage:

<img src="./ncbi_images/ncbi_blast.png" width="800">

By contrast, the dropdown menu:

<img src="./ncbi_images/ncbi_howto_dropdown.png" width="400">

For common some common tool use-case tutorials, select Data and Software:

<img src="./ncbi_images/howto_expanded.png" width="800">

Clicking the how-to guide on downloading the complete genome of an organism takes you to the FTP intro page:

<img src="./ncbi_images/howto_ftp_teaser.png" width="800">

Going back to the front page:

<img src="./ncbi_images/ncbi_home.png" width="800">

The resources column on the left brings you to a more comprehensive list of available all tools and repositories.

<img src="./ncbi_images/ncbi_allresource.png">

On the right hand side are popular resources within the NCBI site. You'll notice that a few of the mentioned above subjects are included in this list.

Content in the center is comprised of links to the main functions of th NCBI site
* Submit: NCBI Submission Portal, for uploading data to their online repositories
* Download: use FTP to bulk download data from NCBI directly to your local machine
* Learn: location for educational materials/tutorials/etc
* Develop: tools and resources for software/web developers, link to NCBI Github repo
* Analyze: find a tool for manipulating, aligning, visualizing, and evaluating biological data
* Research: current tools and basic research topics being worked on by the NCBI Compuational Biology branch

## Core of NCBI: The Entrez Query
Entrez acts as the primary method of executing text queries and retrieval.
It integrates the entire PubMed library of related biomedical literature with a myriad of other relevent literature and moleculare databases. These libraries include:
* DNA + protein sequence + structure
* gene
* genome
* genetic variation
* gene expression

General searches can leave you with an overwhelming number of results, but by using the Entrez search funtion, you can refine your output to a manageable degree.

### If you haven't yet, creating an NCBI account greatly increases the flexibility of the tools and resources at your dispolal through this site.
* A simple example being in working with NCBI's Entrez Programming Utilities:
* With a verified account, your API calls are not throttled, and you're afforded more compute than if you were to remain anonomyous.

NCBI integrates relevent data between databases, meaning if you are examining a Gene Expression Omnibus (GEO) Dataset, a link to the appropriate Profile page will be included.

### Commonly used NCBI Databases

#### Below are a few databases (out of the 39) that NCBI manages

* GEO Database
* SRA
* Genbank
* PubMed + PMC

### Commonly used NCBI Site Utilities

#### A couple useful tools that we'll be covering
* BLAST
* FTP

### Under Development

#### Two resources currently being worked on by NCBI

* NCBI Datasets
* NCBI Virus

## GEO

## SRA
* Contains sequencing data from *all* NGS platforms (Illumna, Roche, etc)
* Largest publicaly available repo of HTS data
* Stores raw sequencing data + alignment information
* Accompanied by SRA-toolkit suite for acquisition + dumping of data from SRA database

## PubMed + PubMed Central
* Biomedical Literature database
* Includes citations + abstracts, from journals such as Nature, Medline, etc
* Wealth of information, however... often paywalled
* PubMed "Vanilla" acts mainly as a reference source, with just the above, citations + abstracts
* PubMed Central however, contains full-text versions of articles for free
* If available, PubMed will link to PMC for appropriate article


## BLAST
* Searches for areas of similarity between biological sequences
* Compares various nucleotide or protein sequences to sequence databases, and calculates statistical significance of matches
* Can determine functional + evolutionary reltionships between sequences
* Identify members of gene families
* Can be ran through a web browser, referenced in external code, installed locally, or executed in a cloud environment through BLAST+ (AWS, Azure, etc)
* There also exist many searches that have been tweaked for specific use cases, such as: 
  * CD-search, which locates conserved domains in submitted sequence
  * Primer-BLAST, which allows you to design primers that are specific to a PCR template (really neat)

## NCBI Datasets (Beta)

<img src="./ncbi_images/ncbi_datasets.png" width="800">

* Resource that NCBI is developing for locating and building datasets
* Allows for bulk downloading of genome sequence as well as matching annotation
* For now, web interface only works with Eukaryotic organisms
* CLI is needed for all other organisms
* As it's still being worked on, content is fairly light 
  * For example, searching for *Mus musculus*, will present you with only a couple reference genomes, and a single available annotation
* As this resource matures, expect usefulness to mature as well

## NCBI Virus (Beta)

<img src="./ncbi_images/ncbi_virus.png" width="800">

* Acts as a central hub of sorts, for viral sequence data originating from GenBank, Refseq, and other NCBI repositories
* Includes a really neat visual aid for the taxonomy of viruses, discriminating between hosts
* Especially relevent today, you can find a link under "Find Data" called "Up-to-date-SARS-Cov2" that brings you to a hub page
* Here you can browse the vast amount of nucleotide and protein data, locate PubMed and PubMed Central pages, perform in-place alignments, and construct a phylogenetic tree