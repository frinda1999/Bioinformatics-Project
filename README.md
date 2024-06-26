# Bioinformatics-Project
The semesterproject of Catherine Rohner and Ann-Sophie Frind for the course 'Bioinformatic Approaches to Epigenetics FS2024'

# Outline

### Format

The project can for example be:

-   Re-producing the analyses from a publication (in a critical fashion)

-   Analyzing new data (e.g. yours or in collaboration with a group)

-   Exploring the differences between a given set of TFs

-   Anything you think of which involves competences developed in the course

# What is the topic?

Using both Chip-seq and ATAC-seq data, we want to investigate histone modifications like H3K4me1 (histone H3 lysine 4 monomethylation) and H3K9me3 (histone H3 lysine 9 trimethylation) in the tissue of left ventricles.
They play essential roles in regulating gene expression, impacting heart development, function, and disease.

1.  **H3K4me1:**

    -   **Role:** Primarily marks enhancers, particularly active ones when found in combination with H3K27ac.

    -   **Relevance:** Important for understanding regulatory elements that might be activated or repressed in an age-dependent manner or between genders in cardiac tissues.

2.  **H3K9me3**:

    -   **Role:** Typically associated with heterochromatin and transcriptional repression.

    -   **Relevance:** Useful for studying regions of the genome that become silenced in an age-dependent manner or differ between genders, potentially impacting cardiac function.Ideas:

#### Aging Differences

Investigate whether aging leads to changes in transcription factor networks and chromatin accessibility in LV tissues, potentially contributing to age-related decline in cardiac function.

#### Gender Differences

Explore differences in transcription factor binding and chromatin accessibility between male and female LV tissues to understand gender-specific risks for cardiac diseases.

# What data will we be using?

We will probably be using these data: <https://www.encodeproject.org/search/?type=Experiment&control_type!=*&status=released&perturbed=false&assay_title=ATAC-seq&assay_title=Histone+ChIP-seq&biosample_ontology.term_name=heart+left+ventricle>

### Old male (73y)

ATAC: <https://www.encodeproject.org/experiments/ENCSR769DGC/>\
H3K4me1: <https://www.encodeproject.org/experiments/ENCSR461MTO/>\
H3K9me3: <https://www.encodeproject.org/experiments/ENCSR843ETK/>\
H3K27ac: <https://www.encodeproject.org/experiments/ENCSR402JWL/>\

### Young male (34y)

ATAC (43y): <https://www.encodeproject.org/experiments/ENCSR310RJN/>\
H3K4me1: <https://www.encodeproject.org/experiments/ENCSR111WGZ/>\
H3K9me3: <https://www.encodeproject.org/experiments/ENCSR176KNR/>\
H3K27ac: <https://www.encodeproject.org/experiments/ENCSR150QXE/>\

### Old female (59y)

ATAC: <https://www.encodeproject.org/experiments/ENCSR925LGW/>\
H3K4me1: <https://www.encodeproject.org/experiments/ENCSR485LPA/>\
H3K9me3: <https://www.encodeproject.org/experiments/ENCSR284DWQ/>\
H3K27ac: <https://www.encodeproject.org/experiments/ENCSR884SIF/>\

### Young female(46y)

ATAC (47y): <https://www.encodeproject.org/experiments/ENCSR399OSE/>\
ATAC (42y): <https://www.encodeproject.org/experiments/ENCSR593YFB/>\
H3K4me1: <https://www.encodeproject.org/experiments/ENCSR848BXL/>\
H3K9me3: <https://www.encodeproject.org/experiments/ENCSR433LHD/>\
H3K27ac: <https://www.encodeproject.org/experiments/ENCSR863BVD/>\

# What are the analyses you wish to reproduce, or the questions you wish to answer?

Generally, the literature suggests that men are generally at higher risk of certain cardiovascular diseases than women.
Also, the risk generally increases with age.
Therefore, we want to see whether we can find differences in the chosen histone modifications between the groups.

1.  **Differential Peak Calling**: Compare peak data between age groups (young vs. old) and between sexes to identify differential binding or chromatin accessibility patterns.

    → Hypothesis: In left ventricle tissue, older individuals have a higher prevalence of H3K9me3 peaks in regions associated with cardiac muscle contraction genes compared to younger individuals, leading to repressive chromatin states and reduced expression of these genes.This differential repressive binding contributes to age-related cardiac functional decline.\
    → Hypothesis: Females exhibit higher chromatin accessibility (ATAC-seq peaks) at H3K4me1-marked enhancers in regions regulating estrogen-responsive genes than males, influencing sex-specific protective effects on cardiac function.

2.  **Gene Association**: Map peaks to the nearest genes or regulatory regions like promoters and enhancers.

    → Hypothesis: Differential H3K4me1 peaks in young vs. old LV tissues are associated with genes involved in oxidative stress response and energy metabolism, implicating age-related enhancer changes in declining mitochondrial function and increased oxidative damage.
    This differential repressive binding contributes to age-related cardiac functional decline.\
    → Hypothesis: Differential H3K9me3 peaks between males and females are linked to genes that regulate inflammatory pathways, suggesting sex-specific repression of pro-inflammatory genes.

3.  **Motif Discovery**: Analyze enriched transcription factor binding motifs in age- or sex-specific peaks.

    → Hypothesis: Age-related H3K4me1 peaks in the LV are enriched for motifs of stress-responsive transcription factors like AP-1 and NRF2, implicating these factors in regulating enhancer activity during cardiac aging.\
    → Hypothesis: Sex-specific chromatin accessibility peaks contain distinct hormone receptor motifs, such as estrogen receptor alpha (ERα) motifs in females, which might explain differential gene regulation related to hormone signaling.

4.  **Co-binding Analysis**: Identify transcription factors potentially co-binding with histone modifications or accessible regions and assess whether their binding differs by age or sex.

    → Hypothesis: In aged LV tissue, the co-binding of H3K9me3 with cardiac transcription factors (e.g., GATA4) at specific promoter regions is reduced compared to young tissue, reflecting a loss of coordinated repression that affects cardiac function.\
    → Hypothesis: Females have distinct transcription factor co-binding patterns at accessible chromatin regions, particularly involving estrogen receptor motifs, influencing gene regulation in a sex-specific manner.\

This is not a final plan, but the start of a discussion!
