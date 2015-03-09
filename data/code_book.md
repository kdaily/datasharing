My data

Experimental design

I'm interested in the gene expression of POU5F1 (commonly known as OCT4) and NANOG in different cell lines when exposed to a drug at different concentrations.

I'm measuring expression using qPCR by combining cells with drug at the different levels in separate wells of a plate. Each well measures expression of a single gene at a single drug amount.

Code book:

CellLine: I used 5 cell lines: C1, C2, C3, C4, and C5 (references for these).

CellType: annotation about the type of cells (references).

I'm using 4 drug amounts - 0 (a control), 0.001, 0.01, and 0.1 ul.
replicate: biological replicates (separate preparations of a cell line)

I ran these 384-well plates on a BioRad qPCR machine.
I copied the raw data files (datafile1.rad, datafile2.rad) to my machine and ran the BioRad software to extract expression values from them. I used the default settings to convert delta Ct values into expression levels.

Notes:

One run of an entire plate failed, and this is marked with a field called 'failed'. 
A few of the wells on the plate failed, and these are blank and annotated with failed. 

