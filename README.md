# BVERSITY INTERNSHIP  
**Project Report: Internship at Bversity**  

---

## Project Goal: Computational Drug Discovery and Molecular Similarity Screening

During my internship at Bversity, I gained practical experience in the early stages of the computational drug discovery pipeline. The main objective was to use modern bioinformatics tools to screen large chemical libraries and identify potential drug candidates. Specifically, I worked on a project focused on finding novel antimalarial leads by performing a molecular similarity search against a known drug, **chloroquine**.

---

## My Contribution & Methodology

I was responsible for building and executing a complete workflow to screen a library of molecules and identify those structurally similar to our query compound. To do this efficiently, I used the **KNIME Analytics Platform**, a powerful tool for creating automated and reproducible bioinformatics workflows.

My workflow involved several key steps:  

- **Data Input:**  
  I started by using SDF Reader nodes to load two separate datasets: a single query molecule (**chloroquine**) and a large library of candidate molecules.

- **Format Conversion:**  
  Next, I used RDKit From Molecule nodes to convert the standard SDF chemical structures into RDKit molecular objects. This is a crucial preparation step for advanced computational analysis.

- **Molecular Fingerprinting:**  
  The core of the analysis was generating molecular fingerprints using RDKit Fingerprint nodes. These fingerprints are digital representations of a molecule's structure, allowing rapid and quantitative comparison. Fingerprints were generated both for the query molecule and every molecule in the library.

- **Similarity Calculation:**  
  Using the Fingerprint Similarity node, I calculated the **Tanimoto similarity coefficient** between chloroquine and each library molecule. This score ranges from 0 to 1, quantifying their structural similarity.

- **Visualization and Analysis:**  
  Finally, I employed a HeatMap (JFreeChart) node to visualize similarity scores, providing an intuitive summary that highlighted molecules with high similarity to chloroquine.

---

## Results & Conclusion

The heatmap analysis revealed that while some molecules had weak-to-moderate similarity to chloroquine (Tanimoto scores in the 0.15–0.2 range), the library did not contain any highly similar molecules. The absence of strong matches (scores > 0.3) indicated that the query molecule was structurally distinct from the compounds in the screened library.

---

## Workflow Visuals  

<img src="images/Cheminformatics Analysis using KNIME.jpg" width="600"/>  
*Cheminformatics analysis workflow implemented in KNIME Analytics Platform.*

<img src="images/Heatmap Representation of Molecules Similar to the Query Molecule.jpg" width="600"/>  
*Heatmap showing similarity scores (Tanimoto coefficients) of library molecules relative to chloroquine.*

---
