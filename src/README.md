# Source Code Organization

This folder contains reusable, production-quality Python modules for the BABS project.

## Folder Structure

### **`/data_processing/`**
Scripts and modules for cleaning, transforming, and preparing raw data.
- Data validation functions
- Normalization and preprocessing pipelines
- Sensor data conversion utilities
- Output: cleaned datasets for analysis

### **`/analysis/`**
Core statistical analysis functions and research algorithms.
- Statistical computations
- Signal processing
- Feature extraction
- Machine learning functions
- Output: analysis results, metrics, trained models

### **`/visualization/`**
Functions for generating plots, diagrams, and publication-ready figures.
- Plotting utilities
- Figure generation
- Diagram creation
- Chart templates
- Output: figures for reports and papers

### **`/utils/`**
Helper functions and utilities used across the project.
- Common constants
- File I/O helpers
- Configuration management
- Logging setup
- Output: reusable utilities imported by other modules

## Best Practices

1. **Write modular, reusable functions** — Not single-use scripts
2. **Include docstrings** — Document all functions, classes, and modules
3. **Follow PEP 8** — Consistent Python style
4. **Add type hints** — Help with code clarity and IDE support
5. **Test critical functions** — Add tests in `/tests/` for core analysis code

## Usage in Notebooks

Import modules from `src/` in your analysis notebooks:

```python
from src.data_processing import normalize_sensor_data
from src.analysis import calculate_statistics
from src.visualization import plot_results
from src.utils import load_config
```

## Contributing

When adding new code:
1. Place in appropriate subfolder based on function
2. Add comprehensive docstrings
3. Consider writing a test for critical functions
4. Update this README if creating new utilities

## See Also

- `/notebooks/` — Jupyter notebooks for exploratory and analysis work
- `/tests/` — Unit tests for code reliability
- `README.md` in parent directory — Overall project structure