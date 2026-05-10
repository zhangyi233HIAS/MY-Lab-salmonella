# DUF1311 key takeaways

##### [**Undermind**](https://undermind.ai)

---


## Table of Contents

- [DUF1311 family key takeaways](#duf1311-family-key-takeaways)
- [Fast read table](#fast-read-table)
- [Absolute key takeaways](#absolute-key-takeaways)
- [Bottom line for the review paper](#bottom-line-for-the-review-paper)
- [References](#references)

## DUF1311 family key takeaways

The recent literature does not treat DUF1311 as a live unknown function family. In practice, the signal has consolidated around the **YefM–YoeB toxin antitoxin module** and closely related YoeB like toxins. The highest value papers show a clear shift from vague annotation to a fairly coherent picture: these proteins are usually stress linked RNases with strong structural conservation, promoter autoregulation through toxin to antitoxin stoichiometry, and species specific phenotypic outputs that matter for biofilm, persistence, and infection (Xue et al. 2020, 2021; Eun et al. 2020; Kim et al. 2024; Qi et al. 2021; Ma et al. 2021; McGillick et al. 2021; Sarah et al. 2025).

## Fast read table

| System and species | Main conclusion | Strongest evidence | Why it matters for the review goal |
|:---|:---|:---|:---|
| **Family level view** | DUF1311 is best reviewed as the **YoeB branch of type II toxin antitoxin systems**, not as an orphan domain. Across recent papers, the family is functionally anchored as a toxin neutralized by YefM and released into stress linked RNA cleavage programs (Xue et al. 2020, 2021; Kim et al. 2024; Qi et al. 2021; Ma et al. 2021). | Repeated structural, biochemical, and genetic treatment under YefM–YoeB labels rather than DUF1311 labels (Xue et al. 2020, 2021; Kim et al. 2024; Qi et al. 2021; Ma et al. 2021). | The review should be organized around **functional reannotation**. Searching only the DUF label would miss most of the important literature. |
| **Staphylococcus aureus** | The best developed pathogen story. YoeB paralogs are structurally resolved, independently regulated, and tied to biofilm formation, antibiotic tolerance, extracellular DNA release, and abscess burden (Eun et al. 2020; Xue et al. 2020, 2021; Qi et al. 2021). | Structural work shows a stoichiometry dependent switch between weakly DNA binding tetramers and strongly DNA binding hexamers (Xue et al. 2020). A second study shows the two paralogs have distinct promoter recognition logic and little cross talk (Xue et al. 2021). Genetics shows yoeB1 or yoeB2 deletion lowers mature biofilm, lowers antibiotic tolerance, and lowers bacterial burden in a mouse abscess model (Qi et al. 2021). | This is the strongest case that the family is not merely a stress module in vitro. In a mammalian pathogen, YefM–YoeB connects regulatory biochemistry to infection relevant phenotypes. |
| **Streptococcus pneumoniae** | The pneumococcal system now has both phenotype and structure. It supports oxidative stress resistance and robust biofilm formation, and the 2024 structure confirms the same core YefM–YoeB architecture seen in other species (Chan et al. 2018; Kim et al. 2024). | Deleting yefM-yoeB reduces survival under hydrogen peroxide and weakens biofilm biomass and viability, with complementation restoring the phenotype (Chan et al. 2018). The TIGR4 complex structure shows a tetramer to hexamer equilibrium and confirms YoeB RNase activity with a promoter binding model centered on YefM DNA recognition (Kim et al. 2024). | This gives a clean bridge from old phenotype work to newer structural mechanism in a major human respiratory pathogen. |
| **Edwardsiella piscicida** | YefM–YoeB clearly affects stress adaptation and host interaction, but the phenotypic direction is not simple. The module improves oxidative stress survival, antibiotic tolerance, and persister formation, yet its deletion can increase serum survival, adhesion, dissemination, and overall virulence in fish (Ma et al. 2021). | Markerless mutants show reduced oxidative stress resistance and reduced antibiotic persistence after deleting the operon, while the same deletion increases biofilm, serum survival, tissue dissemination, and host mortality (Ma et al. 2021). | This is a warning against any single line summary such as “YoeB promotes virulence.” In some pathogens the module behaves more like a brake that balances stress survival against aggressive host exploitation. |
| **Agrobacterium tumefaciens** | YoeB is broader than a classic ribosome locked mRNase. The toxin can cleave both RNA and DNA, with ribosome independent nuclease activity and direct DNA nicking (McGillick et al. 2021). Sequence variation in a short substrate contacting helix helps explain host or species specific toxicity (Ames et al. 2020). | Purified AtYoeB cuts RNA and double stranded DNA with similar dose dependence in the absence of ribosomes, while the ribosome still boosts RNA cleavage efficiency about tenfold (McGillick et al. 2021). Helix swap experiments shift toxicity between Agrobacterium and E. coli hosts (Ames et al. 2020). | This is one of the clearest papers showing that the family has **catalytic plasticity** and species tuned outputs, which helps explain why annotation based on sequence alone stayed uncertain for so long. |
| **Mycobacterium tuberculosis RelK** | A YoeB like toxin in M. tuberculosis extends the family even further: translation inhibition, ribosome independent RNA cleavage, and DNA nicking can all coexist in one toxin (Sarah et al. 2025). | RelK inhibits cell free translation, cleaves RNA and DNA without ribosomes, shows stronger translation inhibition after phosphorylation, and loses both catalytic activity and cytotoxicity when His84 is mutated (Sarah et al. 2025). | This widens the functional horizon of the family beyond a narrow “A site mRNA interferase” view and makes persistence and stress survival in major pathogens a more plausible part of the DUF1311 story. |

## Absolute key takeaways

- **Most important reframing**

  DUF1311 should be treated as a legacy label. The useful biological unit is the **YefM–YoeB module and nearby YoeB like toxins** (Xue et al. 2020, 2021; Kim et al. 2024; McGillick et al. 2021; Sarah et al. 2025).

- **Most important mechanistic conclusion**

  The family is now best supported as a set of **stress linked ribonucleases whose activity and transcription are both controlled by toxin to antitoxin balance**. The strongest structural evidence comes from the stoichiometry dependent tetramer to hexamer switch that governs promoter repression in staphylococci and appears conserved in pneumococcus (Xue et al. 2020, 2021; Kim et al. 2024).

- **Most important pathogen conclusion**

  In mammalian pathogens, especially *S. aureus* and *S. pneumoniae*, YefM–YoeB is tied to phenotypes that matter for persistence in the host, including oxidative stress survival, biofilm integrity, antibiotic tolerance, and local infection burden (Qi et al. 2021; Chan et al. 2018; Kim et al. 2024).

- **Most important caution**

  The family does not produce a single phenotype across species. In *E. piscicida*, the same system that supports stress tolerance can also restrain some host interaction traits, so functional claims must stay species specific (Ma et al. 2021).

- **Most important expansion of function**

  The older picture of YoeB as a narrowly ribosome dependent mRNA toxin is too tight. Work in *A. tumefaciens* and *M. tuberculosis* shows **ribosome independent RNA cleavage and DNA nicking**, which likely reflects latent catalytic breadth in the fold rather than a one off anomaly (McGillick et al. 2021; Sarah et al. 2025).

## Bottom line for the review paper

The strongest current story is not “an unknown domain slowly getting a tentative function.” It is a sharper transition: a legacy DUF label has largely been absorbed into a mechanistically tractable toxin antitoxin family whose core activity is now clear, but whose **physiological role remains context dependent across pathogens**. The best review angle is therefore **from unknown domain to stress linked RNase and regulatory toxin module, with species specific consequences for persistence and virulence** (Qi et al. 2021; Xue et al. 2020; Kim et al. 2024; Ma et al. 2021; McGillick et al. 2021; Sarah et al. 2025).

---

## References

Ames, Jessica R., Julia McGillick, Tamiko Murphy, E. Reddem, and C. Bourne. 2020. “Identifying a Molecular Mechanism That Imparts Species-Specific Toxicity to YoeB Toxins.” *Frontiers in Microbiology* 11 (May). <https://doi.org/10.3389/fmicb.2020.00959>.

Chan, W., Mirian Domenech, Inma Moreno-Córdoba, et al. 2018. “The Streptococcus Pneumoniae yefM-yoeB and relBE Toxin-Antitoxin Operons Participate in Oxidative Stress and Biofilm Formation.” *Toxins* 10 (September). <https://doi.org/10.3390/toxins10090378>.

Eun, Hyun-Jong, Kiyoung Lee, Dong-Gyun Kim, Daseul Im, and Bong‐Jin Lee. 2020. “Crystal Structure of the YoeBSa1-YefMSa1 Complex from Staphylococcus Aureus.” *Biochemical and Biophysical Research Communications* 527 1 (June): 264–69. <https://doi.org/10.1016/j.bbrc.2020.04.089>.

Kim, Do-Hee, Yong-Chan Lee, C. Jin, et al. 2024. “Structural and Functional Insight Into YefM–YoeB Complex of Toxin–Antitoxin System From Streptococcus Pneumoniae.” *Journal of Cellular Biochemistry* 126 (November). <https://doi.org/10.1002/jcb.30672>.

Ma, Dongmei, Han-jie Gu, Yan-jie Shi, Hui-qin Huang, Dong-mei Sun, and Yong-hua Hu. 2021. “Edwardsiella Piscicida YefM-YoeB: A Type II Toxin-Antitoxin System That Is Related to Antibiotic Resistance, Biofilm Formation, Serum Survival, and Host Infection.” *Frontiers in Microbiology* 12 (March). <https://doi.org/10.3389/fmicb.2021.646299>.

McGillick, Julia, Jessica R. Ames, Tamiko Murphy, and C. Bourne. 2021. “A YoeB Toxin Cleaves Both RNA and DNA.” *Scientific Reports* 11 (February). <https://doi.org/10.1038/s41598-021-82950-6>.

Qi, Xinyu, Kimberly M. Brothers, Dongzhu Ma, et al. 2021. “The Staphylococcus Aureus Toxin–Antitoxin System YefM–YoeB Is Associated with Antibiotic Tolerance and Extracellular Dependent Biofilm Formation.” *Journal of Bone and Joint Infection* 6 (July): 241–53. <https://doi.org/10.5194/jbji-6-241-2021>.

Sarah, Shafinaz Rahman, Nimisha Sinha, H. A. Gandhi, Jaydeep Bhattacharya, and Vandana Malhotra. 2025. “RelK, a YoeB-Like Toxin from Mycobacterium Tuberculosis Displays Ribosome Independent Endonucleolytic Activity.” *Biochimica Et Biophysica Acta. Molecular Cell Research*, December 1, 120097. <https://doi.org/10.1016/j.bbamcr.2025.120097>.

Xue, Lu, M. H. Khan, Jian Yue, Zhong-liang Zhu, and L. Niu. 2021. “The Two Paralogous Copies of the YoeB–YefM Toxin–Antitoxin Module in Staphylococcus Aureus Differ in DNA Binding and Recognition Patterns.” *The Journal of Biological Chemistry* 298 (November). <https://doi.org/10.1016/j.jbc.2021.101457>.

Xue, Lu, Jian Yue, J. Ke, et al. 2020. “Distinct Oligomeric Structures of the YoeB–YefM Complex Provide Insights into the Conditional Cooperativity of Type II Toxin–Antitoxin System.” *Nucleic Acids Research* 48 (August): 10527–41. <https://doi.org/10.1093/nar/gkaa706>.
