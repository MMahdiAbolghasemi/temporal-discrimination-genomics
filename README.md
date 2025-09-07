# Binaural Hearing Threshold Analysis with Genetic Markers

## Overview

This repository contains code for analyzing temporal interval discrimination thresholds under different auditory conditions and examining their relationship with genetic variants. The analysis focuses on how genetic polymorphisms in neurotransmitter-related genes affect auditory processing capabilities.

## Description

The project analyzes behavioral data from temporal interval discrimination tasks performed under three conditions:
- **Baseline**: Standard auditory discrimination task
- **Control (Monaural)**: Single-ear auditory processing
- **Binaural**: Both-ear auditory processing

The analysis examines how genetic variants in key neurotransmitter pathway genes influence auditory discrimination thresholds, providing insights into the genetic basis of auditory processing differences.

## Features

- **Data Processing**: Automated loading and cleaning of MATLAB behavioral data files
- **Psychometric Analysis**: Curve fitting and threshold calculation using psychometric functions
- **Statistical Testing**: Wilcoxon signed-rank tests for condition comparisons
- **Genetic Association**: Analysis of genetic variants and their impact on auditory thresholds
- **Visualization**: Comprehensive plotting with statistical annotations

## Requirements

```
numpy
pandas
matplotlib
seaborn
scipy
openpyxl
```

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/binaural-hearing-analysis.git
cd binaural-hearing-analysis
```

2. Install required dependencies:
```bash
pip install numpy pandas matplotlib seaborn scipy openpyxl
```

## Data Structure

The analysis expects the following directory structure:

```
ID_data/
├── all/
│   ├── base/           # Baseline condition .mat files
│   ├── bineural/       # Binaural condition .mat files
│   ├── monoral/        # Monaural condition .mat files
│   └── genome - Copy.xlsx  # Genetic data file
```

### Genetic Markers Analyzed

- **COMT (rs4680)**: Catechol-O-methyltransferase gene variants (AA, AG, GG)
- **SLC6A3 (DAT)**: Dopamine transporter gene (9R9R, 9R10R, 10R10R)
- **HTR2A (rs6313)**: Serotonin 2A receptor gene (CC, CT, TT)
- **SLC6A4**: Serotonin transporter gene (S, S/L, L)
- **ACHEA**: Acetylcholinesterase activity levels

## Usage

### Running the Complete Analysis

```python
from binaural_analysis import run_analysis, plot_genetic_analysis

# Run the main analysis pipeline
results = run_analysis()

# Generate genetic comparison plots
plot_genetic_analysis(results)
```

### Key Functions

- `load_data_from_path()`: Load and process .mat files from directory
- `process_dataframes()`: Clean dataframes by removing empty cells
- `get_correct_answers()`: Filter for correct responses
- `calculate_thresholds()`: Calculate discrimination thresholds using psychometric curve fitting
- `plot_comparison_stats()`: Generate statistical comparison plots

## Analysis Pipeline

1. **Data Loading**: Load behavioral data from .mat files and genetic data from Excel
2. **Data Cleaning**: Remove invalid trials and empty responses
3. **Accuracy Calculation**: Compute psychometric curves from response histograms
4. **Threshold Estimation**: Fit psychometric functions and extract 75% accuracy thresholds
5. **Genetic Association**: Combine behavioral thresholds with genetic variant data
6. **Statistical Analysis**: Compare thresholds across genetic groups using non-parametric tests
7. **Visualization**: Generate publication-ready plots with statistical annotations

## Output

The analysis generates:
- Log-transformed discrimination thresholds for each condition
- Statistical comparisons between genetic groups
- Box plots with significance testing results
- Psychometric curve parameters

## Results Interpretation

- **Lower thresholds** indicate better temporal discrimination ability
- **Significant differences** between genetic groups suggest genetic influence on auditory processing
- **Condition comparisons** reveal the impact of binaural vs. monaural processing


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


```
Abolghsemi, M. M. (2025). Binaural Hearing Threshold Analysis with Genetic Markers. 
GitHub repository: https://github.com/MMahdiAbolghasemi/temporal-discrimination-genomics
```

## Contact

**Author**: M. Mahdi Abolghsemi  
**Email**: [mma.abolghasemi@gmail.com]  
**Date**: July 7, 2025
