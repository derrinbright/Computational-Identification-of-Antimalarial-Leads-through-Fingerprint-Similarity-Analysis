# Computational Drug Discovery by Molecular Similarity Screening Using KNIME  
**Project Status:** Completed  

---

## 1. Project Overview  

This project aimed to apply computational drug discovery techniques to identify novel antimalarial candidates by performing a **molecular similarity screening** against a known drug, **chloroquine**. Using the **KNIME Analytics Platform**, an automated workflow was developed to screen a large chemical library to detect compounds structurally similar to the query molecule.  

The pipeline included data ingestion, molecular fingerprinting, similarity calculation using Tanimoto coefficients, and visual representation of similarity scores. The project provided insights into the structural diversity of the screened chemical library relative to chloroquine.  

---

## 2. Background and Rationale  

### Why This Project?  
Molecular similarity screening is a fundamental tool in early-stage drug discovery. It allows rapid identification of potential drug leads by finding molecules structurally related to known actives. Given the urgent need for novel antimalarial agents, this project focused on discovering new candidates similar to chloroquine, a well-established antimalarial drug.  

Using the KNIME platform enables reproducible, scalable, and visual bioinformatics workflows to process large chemical datasets efficiently.  

---

## 3. Tools and Technologies  

- **Workflow Platform:** KNIME Analytics Platform  
- **Cheminformatics:** RDKit nodes for molecule conversion and fingerprinting  
- **Similarity Metrics:** Tanimoto coefficient via Fingerprint Similarity node  
- **Visualization:** HeatMap (JFreeChart) node for similarity score representation  

---

## 4. Methodology: A Step-by-Step Workflow  

### Phase 1: Data Input and Preparation  
1. Loaded two SDF datasets using **SDF Reader** nodes:  
   - Query molecule: chloroquine  
   - Candidate library: large chemical compound dataset  
2. Converted SDF molecules to computational objects using **RDKit From Molecule** nodes for downstream processing.  

### Phase 2: Fingerprinting and Similarity Calculation  
1. Generated molecular fingerprints with **RDKit Fingerprint** nodes to digitally encode each molecule's structure.  
2. Computed pairwise Tanimoto similarity scores between chloroquine and every molecule in the library using the **Fingerprint Similarity** node.  

### Phase 3: Visualization and Analysis  
Visualized the entire set of similarity scores with the **HeatMap (JFreeChart)** node, allowing quick identification of molecules with varying levels of structural similarity to the query.  

---

## 5. Results and Analysis  

The heatmap revealed only molecules with **weak to moderate similarity** (Tanimoto scores 0.15–0.2) to chloroquine in the library. No highly similar compounds (scores > 0.3) were detected, indicating that the candidate library was largely **structurally distinct** from the query molecule.  

This outcome highlights the uniqueness of chloroquine's chemical scaffold relative to the screened dataset and suggests that further expansion or alternative libraries may be necessary for identifying close analogs.  

---

## 6. Conclusion  

This project successfully implemented a **full cheminformatics workflow** in KNIME for molecular similarity screening and demonstrated that the chosen chemical library contains few compounds structurally related to chloroquine.  

The approach illustrates how KNIME can be leveraged for rapid, automated similarity searches in drug discovery pipelines, providing a reproducible and visual analytic platform to prioritize candidates for further study.  

---

## Workflow Visualizations  

<img src="images/Cheminformatics Analysis using KNIME.jpg" width="600"/>  
*Automated cheminformatics workflow constructed in KNIME.*  

<img src="images/Heatmap Representation of Molecules Similar to the Query Molecule.jpg" width="600"/>  
*Heatmap displaying similarity scores (Tanimoto coefficients) of library molecules versus chloroquine.*  

---
