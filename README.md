Steps to run:

1. Morphological image features are stored in ptc_nuc_feats.rds, a dataset readable in R. Contains nuclear morphology features and clinical information for TCGA patients after quality control/exclusion criteria applied. Original features are stored in OC_feats.mat

2. QuRiS_ptc.Rmd is the markdown file that splits the data into training and test, then assigns risk scores based on the image-based features. Reflected as Mp in the paper.

3. Genomic_QuRiS.Rmd does the same, but with the protein expression RNA-seq genomic data. Reflected as Mg in the paper.

4. Pathogenomic_QuRiS.Rmd as above, but with the prognostic genomic features that were identified through associative analysis and pruning through the image features. The subset of prognostic genes are stored in associated_genes_raw.rds. Reflected as Mg' in the paper.

5. Finally, Morph_Gene_Signature.Rmd combines features in Mp and Mg' to get Mp+g' in the paper. Final risk scores are stored in new_risk_scores_355patients.csv
