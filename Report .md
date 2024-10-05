# **Authors**

Logy Khaled (@Logy), Alaa Hewela (@Alaa253), Tawfek Ahmed Tawfek (@Tawfekahmed25), Rahma mamdouh Mohammed (@Rahmamam2000), Malak Abdelfattah Soula (@Malak), Zeyad Ashraf (@Zashraf03), Nourhan Mahmoud (@NourhanM1) , Mohammed Dahab (@mdahab7)

# **GithubRepo**

https://github.com/Logykh/hackbio-cancer-internship

# **Introduction**

Gliomas are brain tumors with significant heterogeneity, where mutations in the IDH (Isocitrate Dehydrogenase) gene serve as key biomarkers for prognosis and treatment. IDH mutant and wildtype statuses classify gliomas and predict patient outcomes. The study of gene expression data enhances the understanding of molecular differences.

# **Dataset and Preprocessing**

We used gene expression data from the TCGA-LGG cohort, downloaded via TCGABiolinks, and matched with IDH status. Preprocessing involved removing samples with missing IDH status and filtering genes with over 25 zero values. Data normalization ensured consistency for analysis.

# **Results**

Differential expression analysis was conducted using DESeq2 to identify differentially expressed genes between IDH wildtype and mutant gliomas based on an adjusted p-value \< 0.05 and |log2FoldChange| \> 1\. 

The MA plot visualizes the log fold change versus mean normalized counts. Significant outliers indicate potential biomarkers.

![IMG-20241004-WA0030](https://github.com/user-attachments/assets/de7240a3-3a24-455d-9364-32807203641b)

# **Comparison with Target Paper**

Our findings supported the original study’s clustering based on IDH status. However, updated gene expression data suggests that additional clusters may be necessary to uncover more molecular subtypes beyond the six clusters.

# **Conclusion**

The analysis confirms IDH status is crucial in glioma classification using gene expression data. It suggests new glioma subtypes, encouraging further research into biomarkers and refined treatment strategies.  
