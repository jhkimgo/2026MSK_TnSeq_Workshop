# 2026 MSK Tn-seq Workshop

## Galaxy-based Tn-seq Data Analysis

This repository contains the manuals, Galaxy workflows, and example datasets used in the **2026 MSK Tn-seq Workshop**.

The workshop covers the experimental principles of transposon insertion sequencing (Tn-seq) and a practical Galaxy-based workflow for processing Himar/Mariner Tn-seq data, performing TRANSIT analysis, and visualizing genome-wide insertion patterns.

**Instructor:** Wonsik Lee. Ph.D. 

**Sungkyunkwan University (SKKU), School of Pharmacy**

---

## Workshop Overview

### Part 1. Introduction and Construction of a Transposon Insertion Library

- Principles of Tn-seq
- Transposon insertion libraries
- Himar/Mariner transposons and TA insertion sites
- Library complexity and saturation
- Recovery of transposon-genome junctions
- Construction of sequencing-ready Tn-seq libraries

### Part 2. Galaxy-based Tn-seq Data Analysis

Raw sequencing reads are processed to generate genome-wide insertion profiles.

**Analysis overview:**

FASTQ → Quality control → Trimming → Genome mapping → TA-site identification → Read counting → WIG generation

The workflow generates:

- Complete TA-site insertion count tables
- TRANSIT-compatible WIG files
- TRANSIT annotation (`prot_table`)

### Part 3. TRANSIT Analysis

TRANSIT is used for gene-level analysis of Tn-seq insertion profiles.

The practical session includes:

- **Gumbel analysis** for gene essentiality
- **Resampling analysis** for differential fitness between experimental and control conditions
- TTR normalization
- Interpretation of fold changes and statistical significance

### Part 4. Circos Visualization

Galaxy Circos is used to visualize genome-wide Tn-seq results.

The final visualization combines:

- Control TA-site insertion abundance
- Experiment 1 vs Control differential fitness
- Experiment 2 vs Control differential fitness
- Genome coordinates and chromosome position

### Important Notes

The parameters used in these workflows are configured for the example Tn-seq library used in this workshop.

Parameters such as trimming length, mapping criteria, transposon target sequence, and reference genome must be adjusted when analyzing Tn-seq libraries generated using different experimental designs.

---

## Repository Structure

```text
2026MSK_TnSeq_Workshop/
│
├── Manuals/
│   ├── Part1
│   ├── Part2
│   ├── Part3
│   └── Part4
│
├── Workflows/
│   ├── Workflow1_FASTQ_to_TRANSIT_Input
│   ├── Workflow2_TRANSIT_Analysis
│   └── Workflow3_Circos_Visualization
│
├── Example_Data/
│   ├── Workflow1_Input/
│   ├── Workflow2_Input/
│   └── Workflow3_Input/
