
# About

A command line utility to fetch metadata from the NCBI SRA database.

It uses NCBI's Entrez Programming Utilities under the hood to query and retrieve Run-level and Sample-level metadata from the SRA database. Learn more about E-Utilities here: <https://www.ncbi.nlm.nih.gov/books/NBK25499/>

# Usage:

``` bash
sra-metadata-explorer -q QUERY [-o OUTPUT] [-m {quick,full}] [-f] [-h]
```

# Arguments

+-------+------------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| short | long       | default   | help                                                                                                                                                                                                                                                                            |
+:======+:===========+:==========+:================================================================================================================================================================================================================================================================================+
| `-q`  | `--query`  | `None`    | Query string to search the SRA. Please use quotes '' if the query contains multiple words. eg: `PRJNA868738`                                                                                                                                                                    |
|       |            |           |                                                                                                                                                                                                                                                                                 |
|       |            |           | `SRR15736787`                                                                                                                                                                                                                                                                   |
|       |            |           |                                                                                                                                                                                                                                                                                 |
|       |            |           | `'PRJNA761299 OR SRR15736787'`                                                                                                                                                                                                                                                  |
|       |            |           |                                                                                                                                                                                                                                                                                 |
|       |            |           | `'trna[Text Word] AND "Danio rerio"[Organism]'`                                                                                                                                                                                                                                 |
|       |            |           |                                                                                                                                                                                                                                                                                 |
|       |            |           | `'(2008[Publication Date] : 2009[Publication Date]) AND "arabidopsis thaliana"[Organism]'`                                                                                                                                                                                      |
|       |            |           |                                                                                                                                                                                                                                                                                 |
|       |            |           | Please refer <https://www.ncbi.nlm.nih.gov/sra/docs/srasearch/> to learn more about basic and advanced search in NCBI SRA.                                                                                                                                                      |
+-------+------------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `-o`  | `--output` | `output/` | Output directory to store the results. (default: `pwd`)                                                                                                                                                                                                                         |
+-------+------------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `-m`  | `--mode`   | `quick`   | 'quick' mode dumps the run level metadata, whereas 'full' mode attempts to retrieve both the run level and sample level metadata. 'Full' converts the metadata from JSON to CSV for each run accession. 'Full' mode might not work with all complex queries. (default: `quick`) |
+-------+------------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `-f`  | `--fastq`  | `None`    | Locate the web address to the raw data and generate a script to download the fastq file(s). Depending on the number of fastq files to be searched, this can take some time. (default: None)                                                                                     |
+-------+------------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| `-h`  | `--help`   |           | Show this help message and exit.                                                                                                                                                                                                                                                |
+-------+------------+-----------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

## Troubleshooting

-   Check your internet connection.

-   Find the `failed_to_parse.txt` file in the output directory. It contains a list of run accessions that most likely have incorrect or missing metadata in SRA.
