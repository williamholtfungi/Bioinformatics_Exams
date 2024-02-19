
#Loading Packages
if (!require("BiocManager", quietly = TRUE))
  install.packages("BiocManager")
BiocManager::install("Biostrings", force = TRUE)
BiocManager::install("GenomicAlignments", force = TRUE)
library(Biostrings)
library(msa)
library(dplyr)
library(tidyverse)
library(genepop)
library(tidyr)
install.packages("seqinr")
library(seqinr)
library(ape)
install.packages("UniprotR")
install.packages("protti")
install.packages("r3dmol")
library(UniprotR)
library(protti)
library(r3dmol)
library(snakecase)
remotes::install_github("Tazinho/snakecase")
install.packages("protti", dependencies = TRUE)


#Directory Check
getwd()

#Importing 20 Sequences
mySequences <- Biostrings::readDNAStringSet("sequences.fasta")

#MSA alignment
myFirstAlignment <- msa::msa(mySequences)
myFirstAlignment

print(myFirstAlignment, show="complete")

#Importing the "Most Different Sequence"
Sequence06 <- Biostrings::readDNAStringSet("sequence06.fasta")


#Translating Sequence06 into AA
aa_sequence <- Biostrings::translate(Sequence06)
aa_sequence
as.character(aa_sequence)

#AA Sequence to a FASTA file
output_file <- "amino_acid_sequence.fasta"
Biostrings::writeXStringSet(aa_sequence, file = output_file,
                format = "fasta", width = 60)








