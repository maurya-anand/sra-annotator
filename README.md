# About

A command-line tool for retrieving annotations from the NCBI SRA database.

It uses NCBI's Entrez Programming Utilities under the hood to query and retrieve Run-level and Sample-level metadata from the SRA database. Learn more about E-Utilities here: <https://www.ncbi.nlm.nih.gov/books/NBK25499/>

# Installation:

    pip install -r requirements.txt

# Quick start:

    sra-annotator -q <QUERY> [-o <OUTPUT>] [-m <quick or full>] [-f] [-h]

- `-q` is mandatory

- arguments shown in `[]` are optional

# Usage details:

Checkout the [Wiki page](https://github.com/maurya-anand/sra-metadata-explorer/wiki "Wiki") for more details.
