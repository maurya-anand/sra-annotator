# About

A command-line tool for retrieving annotations from the NCBI SRA database.

It uses NCBI's Entrez Programming Utilities under the hood to query and retrieve Run-level and Sample-level annotation from the SRA database. Learn more about E-Utilities here: <https://www.ncbi.nlm.nih.gov/books/NBK25499/>

# Installation:

    pip install -r requirements.txt

# Quick start:

    sra-annotator [-q] [-o OUTPUT] [-m {quick,full}] [-f] [-d DICTIONARY] [-v] [-h] query

- User must specify a query term or use `-q` to input a list of SRA accessions. An input file or search keyword is required.

- arguments shown in `[]` are optional.

# Usage details:

Checkout the [Wiki page](https://github.com/maurya-anand/sra-annotator/wiki "Wiki") for more details.
