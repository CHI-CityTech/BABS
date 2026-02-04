# Jupyter Notebooks

This folder contains Jupyter notebooks for research exploration, analysis, and reporting.

## Folder Structure

### **`/exploratory/`**
Initial data exploration and prototyping notebooks.
- First look at datasets
- Data quality assessment
- Hypothesis generation
- Preliminary visualizations
- Speculative analysis

**Naming convention:** `01_description_YYYY-MM-DD.ipynb`
Example: `01_sensor_data_exploration_2026-02-04.ipynb`

### **`/analysis/`**
Main research analysis and statistical work.
- Hypothesis testing
- Detailed statistical analysis
- Signal processing
- Feature engineering
- Model development and validation

**Naming convention:** `02_description_v1.ipynb`
Example: `02_heart_rate_statistical_analysis_v1.ipynb`

### **`/reporting/`**
Publication-ready outputs for papers, reports, and presentations.
- Final figures and tables
- Summary statistics
- Research conclusions
- Results documentation
- Polished visualizations

**Naming convention:** `03_description_final.ipynb`
Example: `03_phase1_results_final.ipynb`

## Best Practices

1. **Use clear, descriptive filenames** — Should indicate notebook purpose
2. **Include markdown documentation** — Explain analysis steps, assumptions, results
3. **Restart and run all cells** — Verify reproducibility before committing
4. **Remove debugging code** — Clean up before version control
5. **Import from `/src/`** — Use reusable modules, not inline code

Example structure:
```python
# Import reusable modules
from src.data_processing import load_and_normalize
from src.analysis import compute_statistics
from src.visualization import plot_results

# Load and prepare data
data = load_and_normalize('raw_sensor_data.csv')

# Perform analysis
results = compute_statistics(data)

# Visualize
plot_results(results)
```

## Exporting Notebooks

For sharing with advisors or publication:
- Export to **HTML**: `File → Download As → HTML`
- Export to **PDF**: `File → Download As → PDF`
- Export to **Markdown**: For inclusion in reports

## SRDMPA Alignment

- **Speculate/Research** → Exploratory notebooks
- **Design/Make** → Analysis notebooks
- **Publish/Assess** → Reporting notebooks

## See Also

- `/src/` — Reusable analysis code to import
- `/data/` — Raw and processed datasets
- `/docs/` — Research documentation and guides
2. Remove or comment out debugging code
3. Restart and run all cells before committing
4. Keep notebooks focused on a single topic
5. Export final notebooks to HTML/PDF for sharing