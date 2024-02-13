---
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

# Projects and Tools

## Sustainability
### Predicting per-ship maritime carbon emissions]
Maritime shipping accounts for roughly 2% of all global carbon emissions from human activity, and rose 29% between 2015 and 2020. The roughly 30,000 ships that dock in the European Union in a given year are now required to report their efficiency (kilograms of CO2 per nautical mile), but the efficiency of most of the remaining 100k+ large ships remains undisclosed. We are developing a machine learning model that learns from ships with known efficiency to predict unknown efficiency on a per-ship basis using available ship metadata. The code can be seen here: <https://github.com/knights-lab/climate-trace-shipping>.

### ERMIN: emissions reporting data standard
Global tracking of carbon emissions at the asset level is essential to holding producers accountable for doing their part to reduce emissions. Many efforts are under way to automate collection and reporting of emissions from all sectors of human activity, but we are currently lacking well-defined data standards for emissions reporting. The Emissions Report Minimum INformation (ERMIN) data standard is designed to allow producers and monitoring groups to report asset-level emissions using the UNFCCC Annex 1 categorization of human-related emissions in such a way that data can be easily integrated across inventories and sectors. This standardization is intended to help downstream users access and analyze comprehensive emissions data sets without having to manually parse and align different reporting formats. The ERMIN standards and software tools for validation can be found here: <https://github.com/knights-lab/ermin-standards>.

## Bioinformatics
### Local Manifold Distance (LMdist)
A common approach to analyzing high-dimensional microbiome data is beta diversity analysis. This is usually visualized with dimensionality reduction like principal coordinates analysis (PCoA), which removes redundancy in a dataset to show the major sources of variation in two or three dimensions. Ecological beta diversity has long been affected by apparent geometric abnormalities known as the “arch” or “horseshoe” effects that occur when the primary source of variation is a long continuous geochemical or environmental gradient. We have found that the arch effect is a result of the fundamental limitation in dynamic range of beta diversity measures, and not an issue with the dimensionality reduction. When a dataset includes samples from highly disparate ecosystems at opposite ends of a gradient, typical ecological distance metrics cannot distinguish between "far apart" and "very far apart". This leads to the “arch effect” or more extreme “horseshoe effect.” To overcome this limitation of beta diversity metrics in measuring very long distances, we are developing a method called local manifold distance (LMdist), which relies only on small, local distances to measure beta diversity. LMdistw development was led by Suzie Hoops. See manuscript [here](https://academic.oup.com/bioinformatics/article/39/12/btad727/7461183).

### FoodTree
Traditional dietary intake analyses typically rely on broad food groups or nutrient analysis to overcome the highly individualized nature of modern human diets. These approaches fail to account for food-specific variation in complex fibers and other compounds that may affect the gut microbiome. FoodTree places foods into a tree structure, enabling the use of tree-based analysis methods like UniFrac and phylogenetic diversity that share statistical signal across related features. FoodTree was led by Dr. Abby Johnson. FoodTree tree and code are available here: <https://github.com/knights-lab/Food_Tree>.

### SHOGUN
The software pipeline SHOGUN profiles known taxonomic and gene abundances of short-read shotgun metagenomics sequencing data. The pipeline is scalable, modular and flexible. Data analysis and transformation steps can be run individually or together in an automated workflow. Users can easily create new reference databases and can select one of three DNA alignment tools, ranging from ultra-fast low-RAM k-mer-based database search to fully exhaustive gapped DNA alignment, to best fit their analysis needs and computational resources. The pipeline includes an implementation of a published method for taxonomy assignment disambiguation with empirical Bayesian redistribution. The software is installable via the conda resource management framework, has plugins for the QIIME2 and QIITA packages and produces both taxonomy and gene abundance profile tables with a single command, thus promoting convenient and reproducible metagenomics research. SHOGUN development and maintenance is led by Dr. Ben Hillmann. SHOGUN is available here: <https://github.com/knights-lab/shogun>.

### SplinectomeR
Longitudinal, prospective studies often rely on multi-omics approaches, wherein various specimens are analyzed for genomic, metabolomic, and/or transcriptomic profiles. In practice, longitudinal studies in humans and other animals routinely suffer from subject dropout, irregular sampling, and biological variation that may not be normally distributed. As a result, testing hypotheses about observations over time can be statistically challenging without performing transformations and dramatic simplifications to the dataset, causing a loss of longitudinal power in the process. SplinectomeR is an R package that uses smoothing splines to summarize data for straightforward hypothesis testing in longitudinal studies. The package is open-source, and can be used interactively within R or run from the command line as a standalone tool. SplinectomeR development was led by Dr. Robin Shields-Cutler. SplinectomeR is available here: <https://github.com/RRShieldsCutler/splinectomeR>.

### BURST
BURST is an optimal DNA alignment tool capable of running up to 10,000 times faster than standard implementations of the Needleman-Wunsch alignment method, without sacrificing optimality, when run on large input data sets containing short-read DNA sequencing data. This speedup is achieved by pruning the search space, leveraging redundancies in the input data, and using finely tuned C and assembly code optimizations. BURST can return all tied best hits in a DNA search, or all hits above a certain identity threshold. BURST development was led by Dr. Gabe Al-Ghalith. BURST is available here: <https://github.com/knights-lab/BURST>.

### SHI7
SHI7 (pronounced "shizen") is a user-friendly quality control pipeline, which aims to simplify quality control of short-read data for the end user by predicting presence and/or type of common sequencing adaptors, what quality scores to trim, whether the data set is shotgun or amplicon sequencing, whether reads are paired end or single end, and whether pairs are stitchable, including the expected amount of pair overlap. SHI7 development was led by Dr. Gabe Al-Ghalith. SHI7 is available here: <https://github.com/knights-lab/shi7>.

### NINJA-OPS
NINJA-OPS is a recursive acronym that stands for "NINJA Is Not Just Another - OTU Picking Solution". Making use of BWT-enabled aligners, NINJA quickly generates a QIIME-compatible closed-reference OTU table from a given fasta file of sequence reads. NINJA also allows for convenient quality control on your data, such as fast reverse complementing, base pair trimming, and a specialized denoising transformation. Moreover, NINJA is entirely free and open source. NINJA is 5-10 times faster than USEARCH, and produces more accurate OTU assignments. NINJA can convert an entire MiSeq run of human microbiome amplicon data into a taxonomy-annotated OTU table in around 10 minutes on a laptop. NINJA-OPS development was led by Dr. Gabe Al-Ghalith. The latest NINJA version can always be found on the [Github repo](https://github.com/knights-lab/NINJA-OPS), or at <http://ninja-ops.ninja>. 

### BugBase
BugBase is an analysis tool for 16S datasets. BugBase estimates high-level community-wide microbiome phenotypes including: Gram Staining, Biofilm Formation, Pathogenicity, Mobile Element, and Oxygen Tolerance. The latest BugBase version can always be found on [Github](https://github.com/knights-lab/BugBase). An interactive web-based version is available at <http://bugbase.cs.umn.edu>. Upload your closed-reference Greengenes 13.8 QIIME-compatible OTU table in BIOM format and get back a table of the estimated prevalence of these traits in each sample. BugBase development was led by Dr. Tonya Ward.

### QIIME
QIIME is a large, complex software pipeline with many contributors, led by the labs of Greg Caporaso and Rob Knight. Knights Lab members have contributed plugins, design ideas, and core functionality to QIIME. QIIME (canonically pronounced "chime") stands for Quantitative Insights Into Microbial Ecology. QIIME and QIIME2 are open-source bioinformatics pipelines for performing microbiome analysis from raw DNA sequencing data. QIIME2 is designed to take users from raw sequencing data generated on the Illumina or other platforms through publication quality graphics and statistics. This includes demultiplexing and quality filtering, OTU picking, taxonomic assignment, and phylogenetic reconstruction, and diversity analyses and visualizations. QIIME2 has been applied to studies based on billions of sequences from tens of thousands of samples. Find download links at more at <qiime2.org>.

### SourceTracker
SourceTracker uses Bayesian statistics to predict the source of microbial communities in a set of input samples (i.e., the sink samples). See some uses of SourceTracker for inspiration [here](https://scholar.google.com/scholar?cites=4177367334620506079&as_sdt=5,24&sciodt=0,24&hl=en). SourceTracker development was led by Dr. Knights. Download the latest version from the [Github repo](https://github.com/danknights/sourcetracker). Read a tutorial and more at [qiime.org](http://qiime.org/tutorials/source_tracking.html). Citation: Knights D, Kuczynski J, Charlson E, Zaneveld J, Collman RG, Bushman FD, Knight R, Kelley ST. (2011). Bayesian community-wide microbial source tracking. Nature Methods. 2011 Jul 17.

### Other software tools led by Gabe Al-Ghalith
* [aKronyMer](https://github.com/knights-lab/aKronyMer): De novo phylogeny and database-free metagenomic sample comparison and diversity calculation
* [BURST](https://github.com/knights-lab/BURST): Optimal short-read alignment for metagenomic shotgun and amplicon data
* [NINJA-OPS](https://github.com/knights-lab/NINJA-OPS): Heuristic short-read alignment for amplicon data
* [SHI7](https://github.com/knights-lab/shi7): Self-learning quality control for short-read (metagenomic) fastq sequence data
* [UTree](https://github.com/knights-lab/UTree): Heuristic short-read assignment for metagnomic shotgun and amplicon data
* [Kafan](https://github.com/knights-lab/kafan): Compression for biological sequence data faster and more efficient than gzip
* [EMBALMLETS](https://github.com/knights-lab/BURST/tree/master/embalmlets/bin): Miscellaneous tools for metagenomic sort-read processing: 
* [LLsim](https://github.com/knights-lab/BURST/tree/master/embalmlets/bin): short-read simulator with specific error control from multi-sequence fasta inputs
* [embalmulate](https://github.com/knights-lab/BURST/tree/master/embalmlets/bin): converter for burst/.b6 output into QIIME1 OTU table
* [bcov](https://github.com/knights-lab/BURST/tree/master/embalmlets/bin): coverage analyzer for burst/.b6 output
* [lingenome](https://github.com/knights-lab/BURST/tree/master/embalmlets/bin): prepares genomic database out of a folder of NCBI assemblies
* [t2gg/a2gg](https://github.com/knights-lab/BURST/tree/master/embalmlets/bin): taxonomy annotation toolkit for NCBI genome/gene assemblies
* [WRANGLr](https://github.com/GabeAl/WRANGLr): microbial coalition creation using Nei-Saitou-guided tree of pairwise feature recombination
* [Gabe's DBs](https://github.com/knights-lab/BURST/tree/master/embalmlets): pipeline to automate the creation of new amplicon, WGS, and gene databases from NCBI RefSeq representative sequences
