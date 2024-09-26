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

