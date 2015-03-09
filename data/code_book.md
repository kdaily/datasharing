# My data

## Experimental design

I'm interested in the gene expression of POU5F1 (commonly known as OCT4) and NANOG in different cell lines when exposed to a drug at different concentrations.

I'm measuring expression using qPCR by combining cells with drug at the different levels in separate wells of a plate.
Each well measures expression of a single gene at a single drug amount.

## Code book

### Sample Info table

CellLine: I used 5 cell lines: C1, C2, C3, C4, and C5 (references for these).
CellType: annotation about the type of cells (references).

### Run info table

replicate: biological replicates (separate preparations of a cell line)
date: the date I ran this experiment
failed: if the entire run failed due to some unkown issue with the BioRad qPCR machine.

### Data table

Includes the CellLine, Replicate, and failed.

Amount: amount of drug (0 (a control), 0.001, 0.01, and 0.1 ul)

Gene: POU5F1 and NANOG

row: row of the plate
column: column of the plate
expression: summarized expression level computed by BioRad software
expressionCensored: this particular well failed to work

## Steps

1. I ran these 384-well plates on a BioRad qPCR machine.
2. I copied the raw data files (datafile1.rad, datafile2.rad) to my machine and ran the BioRad software to extract expression values from them (resulting in datafile1.txt and datafile2.txt). I used the default settings to convert delta Ct values into expression levels.
3. I compiled the data table using these values by manually manipulating the data files.

## Notes:

One run of an entire plate failed, and this is marked with a field called 'failed'. 

A few individual wells also failed, and these are marked by a column `expressionCensored`.

