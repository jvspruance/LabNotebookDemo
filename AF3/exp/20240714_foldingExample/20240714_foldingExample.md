# Reviewing an example of folding two proteins together

## Background/Introduction

As a basic example, I want to compare protein complex structures for EIF4EBP1 + EIF4E and phospho-EIF4EBP1 + EIF4E. In order to do this, I need to grab FASTA files for each protein and annotate EIF4BP1 with its associated phosphosites.

In these notes, I will explain how I got data and folded sequences

## Objective(s)

- Extract FASTA files for my proteins of interest for protein folding
- Identify common phosphosites in EIF4EBP1
- Fold protein complexes using AF3

## Materials/Methods

See AF3 server account; FASTA sequences (and phosphosites) are logged there with each AF3 run. 

## Results

- Results are deposited [here](../../results/20240714_fold_protein_complex)

## Conclusions

It's a little too hard to jump to any conclusions regarding this analysis as I only looked at one structure. I should probably cross-reference my AF3 structures with those derived in the PDB.

It could be potentially more interesting to do this in the future with a larger number of known interactions between phosphorylated/unphosphorylated proteins and their binders, but this is somewhat untenable given the current rate limits with running AF3.