# Get_gene_co-ordinates
## About
Get_gene_co-ordinates is a Python script designed for obtaining gene co-ordinates from the output of the Tuxedo suite of tools for RNA-seq analysis [(Trapnell *et al.*, 2012)](http://www.nature.com/nprot/journal/v7/n3/full/nprot.2012.016.html) for genes of interest, though it could also be used on gtf files from other sources. This might be useful for e.g. comparing the co-ordinates of predicted genes to those of annotated genes, to identify genes where the annotation may be incomplete.

## Citation
To cite RNA-seq_analysis tools, please cite the following paper: [Sutton ER, Yu Y, Shimeld SM, White-Cooper H, Alphey L: Identification of genes for engineering the male germline of *Aedes aegypti* and *Ceratitis capitata*. BMC Genomics 2016 17:948.](https://www.ncbi.nlm.nih.gov/pubmed/27871244)

## Requirements
Get_gene_co-ordinates requires Python. It has been tested only with Python 2.7.3.

## Usage
Get_gene_co-ordinates has two required arguments, detailed below.

### *Required arguments*
* `gtf` - path to gtf file
* `genes` - path to text file containing list of genes (in a single column) for which transcript sequences are desired 

### *Example*
To obtain gene co-ordinates for selected genes, the command might be:

    ./get_gene_co-ordinates.py -gtf merged.gtf -genes genes.txt

## Output
Get_gene_co-ordinates produces one output file, called `gene_co-ordinates.bed`. This is a BED file containing co-ordinates for all the genes listed in the input text file.
