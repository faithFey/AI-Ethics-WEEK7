
# COMPAS Recidivism Dataset Bias Audit

## Overview
This project audits the COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) Recidivism Dataset for racial bias using IBM's AI Fairness 360 toolkit. The analysis focuses on identifying disparities in risk score predictions across different racial groups.

## Objectives
1. **Bias Detection**: Analyze racial bias in COMPAS risk scores using statistical fairness metrics
2. **Data Visualization**: Create compelling visualizations showing disparities in false positive rates and other key metrics
3. **Documentation**: Produce a comprehensive 300-word report with actionable remediation strategies

## Dataset Information
- **Source**: COMPAS Recidivism Dataset (ProPublica)
- **Size**: ~7,000 criminal defendants from Broward County, Florida
- **Key Features**: Demographics, criminal history, COMPAS risk scores, actual recidivism outcomes
- **Protected Attribute**: Race (African-American vs. Caucasian)
- **Target Variable**: Two-year recidivism rate

## Technical Stack
- **Python 3.8+**
- **AI Fairness 360 (AIF360)**: IBM's comprehensive bias detection and mitigation toolkit
- **Pandas**: Data manipulation and analysis
- **Matplotlib/Seaborn**: Statistical visualizations
- **NumPy**: Numerical computations
- **Jupyter Notebook**: Interactive development environment

## Installation Requirements
```bash
pip install aif360
pip install pandas matplotlib seaborn numpy jupyter
pip install scikit-learn
```

## Key Fairness Metrics to Analyze
- **Statistical Parity**: Equal positive prediction rates across groups
- **Equalized Odds**: Equal true positive and false positive rates
- **Calibration**: Equal positive predictive values
- **Individual Fairness**: Similar predictions for similar individuals

## Expected Deliverables

### 1. Data Analysis Script (`bias_audit.py`)
- Load and preprocess COMPAS dataset
- Apply AIF360 bias detection metrics
- Calculate disparate impact ratios
- Perform statistical significance tests

### 2. Visualization Suite
- **False Positive Rate Comparison**: Bar charts showing FPR by race
- **Risk Score Distribution**: Histograms comparing score distributions
- **Confusion Matrix Heatmaps**: Visual representation of prediction accuracy by group
- **Fairness Metrics Dashboard**: Comprehensive metric comparison

### 3. Technical Report (`findings_report.md`)
**Structure (300 words):**
- **Executive Summary** (75 words): Key findings and bias magnitude
- **Methodology** (50 words): AIF360 tools and metrics used
- **Results** (100 words): Quantified bias measurements and statistical significance
- **Remediation Strategies** (75 words): Specific technical solutions (re-weighting, post-processing, algorithmic debiasing)

### 4. Jupyter Notebook (`compas_analysis.ipynb`)
- Interactive exploration of bias patterns
- Step-by-step methodology documentation
- Reproducible analysis pipeline

## Project Structure
```
compas-bias-audit/
├── README.md
├── data/
│   └── compas-scores-two-years.csv
├── notebooks/
│   └── compas_analysis.ipynb
├── src/
│   └── bias_audit.py
├── visualizations/
│   ├── fpr_comparison.png
│   ├── risk_distribution.png
│   └── fairness_dashboard.png
└── reports/
    └── findings_report.md
```

## Expected Findings
Based on existing research, the audit will likely reveal:
- Higher false positive rates for African-American defendants
- Significant disparate impact in risk score assignments
- Violations of multiple fairness criteria
- Need for bias mitigation interventions

## Usage Instructions
1. Clone the repository and install dependencies
2. Download COMPAS dataset to `data/` directory
3. Run `python src/bias_audit.py` for automated analysis
4. Open `notebooks/Audit a Dataset for Bias.ipynb` for interactive exploration
5. Review generated visualizations in `visualizations/` folder
6. Read comprehensive findings in `reports/findings_report.md`

## Ethical Considerations
This audit addresses critical issues in algorithmic fairness within the criminal justice system. The findings will contribute to ongoing discussions about bias in predictive policing and risk assessment tools, with potential impacts on real-world sentencing and parole decisions.

## References
- Angwin, J., et al. "Machine Bias." ProPublica, 2016
- IBM AI Fairness 360 Documentation
- Barocas, S., Hardt, M., Narayanan, A. "Fairness and Machine Learning" (2019)

