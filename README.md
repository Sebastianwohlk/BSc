# BSc
This repository serves as appendices for my bachelor's thesis.

Here, you will be able to find my pipeline and validation thereof in html and rmd formats.
Additionally, I have uploaded a flowchart explaining the pipeline as well as an example dataset.

[Pipeline and Correlations as HTML files for your viewing pleasure](https://sebastianwohlk.github.io/BSc/)

![Flowchart of pipeline](https://user-images.githubusercontent.com/77670585/105363794-b7e42300-5bfc-11eb-964c-bf4f14849dc0.jpg)

### Walkthrough of the pipeline

For the script **Pipeline_final_anon.Rmd** you will need a phyloseq and a FASTA input.
If following the example given here - use *phyloseq_anon.RData* and *zOTUs.txt*.

This will provide you with the outputs *diagonal_matrix.csv* and *zOTUs.fasta*.
Both will be located in your working directory.

**These files must be manually uploaded to [the Piphillin server](https://piphillin.secondgenome.com/) and downloaded from the provided email**.

If following the example given here, there results are already uploaded to save you the trouble.
Find it as *ko_genome_contribution_table.RData*.

Through the KEGGLink API, genome contribution is filtered by biological relevance.
A new file is saved to your working directory - *Inferred_zOTU_to_compound_relation.RData*.
This file will be used for validation through correlations.

The rest of the pipeline contains some descriptive statistics of your results.

An example of this can be found in [the HTML version of the pipeline](https://sebastianwohlk.github.io/BSc/Pipeline_final_anon.html).

### Walkthrough of the validation

For the script **Correlations_final_anon.Rmd** you will first need a phyloseq and a metabolite data input.
If following the example given here - use *phyloseq_anon.RData* and *GC_targeted_KEGGID.xlsx*.
These will then be correlated.

Afterwards, load your genome contribution from before.
If following the example given here - use *Inferred_zOTU_to_compound_relation.RData*.

The pairwise correlation coefficients between metabolites and compounds are correlated again.
This time to the amount of KEGG database links.

An example of this can be found in [the HTML version of the validation](https://sebastianwohlk.github.io/BSc/Correlations_final_anon.html).
