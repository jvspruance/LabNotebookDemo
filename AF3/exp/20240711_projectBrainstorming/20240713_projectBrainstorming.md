# Exploring what's new with AlphaFold3

## Background/Introduction

Protein-folding algorithms have been around for a couple of years now, but up until recently, we haven'e been able to fold protein and nucleic acids together, or even proteins with distinct post-translational modifications.

AlphaFold3 addresses this gap by allowing users to fold multiple molecules at once, and those molecules can have PTMs or non-canonical nucleotides. Additionally, the model is newly able to handle 5000 amino acids at once. We can newly fold very large proteins.

I will spend this space brainstorming experiments that I can design with the new AlphaFold3 model, with the expectation that the model will become open source and it will become easy to automate folding soon. I will also spend time thinking about basic test cases I can use to get familiar with model outputs.

## Objective(s)

- Brainstorm potential experiments we can try with AlphaFold3
- Start playing around with AlphaFold3

## Materials/Methods

Citation for AF3:

1. Abramson, J. et al. Accurate structure prediction of biomolecular interactions with AlphaFold 3. Nature 630, 493–500 (2024).

I registered for an account [here](<https://alphafoldserver.com/>) to access the AF3 beta.

### What kinds of things could be cool to model with AF3?

A lot of previous work has been done to analyze how SNVs affect how AlphaFold folds a sequence. In fact, AlphaFold is oftentimes not very sensitive to SNVs, and the structures do not change significantly in their presence. 

Is AlphaFold3 any more sensitive to SNVs than previous models? Similarly, how do small changes (like PTMs or RNA modifications) affect protein-protein binding or protein-RNA binding?

### 2024.07.13

Phosphorylation is a relatively common PTM involved in cell signaling. The negatively charged phosphate group, when attached to a serine, threonine, or tyrosine, can induce strong conformational changes on a protein and affect its function.

To get started, I will take a look at a protein complex structure between a protein that is only known to bind another protein when phosphorylated.

1. Gebauer, F. & Hentze, M. W. Molecular mechanisms of translational control. Nat Rev Mol Cell Biol 5, 827–835 (2004).
1. Musa, J. et al. Eukaryotic initiation factor 4E-binding protein 1 (4E-BP1): a master regulator of mRNA translation involved in tumorigenesis. Oncogene 35, 4675–4688 (2016).


As an example, I will look at the interaction between EIF4EBP1 and EIF4E. When phosphorylated, EIF4EBP1 is unable to bind EIF4E, which facilitates translation. However, when EIF4EBP1 is not phosphorylated, it binds to EIF4E and hinders translation initiation.

Given the significant functional impact of EIF4EBP1 phosphorylation on its binding to EIF4E, I hypothesize that the predicted structures for phospho-EIF4EBP1 + EIF4E and EIF4EBP1 + EIF4E will be qualitatively different; I think that observing small examples like this might give me a good idea of how to quantify differences.
