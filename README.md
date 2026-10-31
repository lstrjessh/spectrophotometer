# Portable Spectrophotometer

Software for capturing spectra, analyzing absorbance, and training concentration-prediction models. Built alongside a portable CMOS camera-based spectrophotometer for heavy metal analysis as part of an undergraduate thesis.

![Desktop capture view](images/capture_view.png)

## Features

- Camera capture with wavelength calibration, smoothing, and spectrum export.
- Absorbance calculation and comparison of spectral CSV files.
- Regression model training, cross-validation, and concentration prediction.
- Model and preprocessing export for reuse with new measurements.

Desktop interface: **PyQt6**. Web interface: **Streamlit**. Modeling: **scikit-learn, PyTorch, XGBoost**.

## Run

From the repository root, install the shared dependencies:

```bash
python -m pip install -r requirements.txt
```

For the desktop app, install its additional dependencies and launch:

```bash
python -m pip install PyQt6 matplotlib opencv-python
python -m qt_app.main_qt
```

Or launch the web app:

```bash
streamlit run Main.py
```

Use CSV files containing wavelength and intensity or absorbance columns. For calibration, enter concentrations manually or include them in filenames, such as `0.5_a.csv`. Example files are in [sample_data/](sample_data/).

## Research

[Read the paper](https://dx.doi.org/10.2139/ssrn.7397594).
