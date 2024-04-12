# Assignment 4: Binding Site Identification in E. coli
Author: Saranya Guvvala

# Date: 04/12/2024

# Programming Language & Version
Python 3.8

# Dependencies
numpy
bz2

# Input
E_coli_K12_MG1655.400_50.bz2: Contains the upstream regulatory regions of genes in E. coli in a compressed format.
argR-counts-matrix.txt: Contains the counts matrix for the transcription factor argR binding sites.

# Script Description:
This Python script calculates the Position Weight Matrix (PWM) for the transcription factor argR and scans the upstream regulatory regions of E. coli genes to identify potential binding sites. It uses a pseudocount to avoid logarithms of zero in PWM calculation and adjusts the counts matrix to ensure stable frequency estimates. The script efficiently processes the compressed input data and extracts binding sites based on their PWM scores, showcasing the top scoring sites.

# Output
PWM (Position Weight Matrix): A matrix printed in the console that represents the likelihood of each base (A, C, G, T) occurring at each position in a potential argR binding site.

Adjusted Frequency Matrix F'(b, j) with Pseudocounts: This matrix is printed in the console as well and shows the frequency of each base at each position after adjusting for pseudocounts.

Top 30 binding sites: The console output will list the top 30 potential binding sites ranked by their PWM scores. Each listed binding site will include the gene ID, the score calculated by the PWM, the position within the upstream region, and the sequence of the binding site.
