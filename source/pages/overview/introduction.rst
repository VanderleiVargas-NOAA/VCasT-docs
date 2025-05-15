Introduction to VCasT
=====================

VCasT (Verification and Forecast Evaluation Tool) is a Python-based library designed to compute, aggregate, and analyze statistical metrics for the evaluation of weather forecasts. It provides a flexible and extensible framework for verifying both deterministic and probabilistic forecasts across various spatial and temporal scales.

Developed at NOAA’s Global Systems Laboratory (GSL) in collaboration with CIRA at Colorado State University, VCasT is intended for research, development, and operational applications in numerical weather prediction.

What VCasT Does
---------------

VCasT enables users to:

- Compute a wide range of verification metrics such as RMSE, MAE, bias, CSI, POD, FAR, GSS, FBIAS, Brier Score, correlation, and more
- Filter forecast-observation pair data by time, variable, model, thresholds, lead time, and domain
- Aggregate scores across user-defined groupings (e.g., by forecast lead time or region)
- Compare the performance of multiple forecasts through pairwise statistical testing
- Generate data-ready outputs for visual analysis or reporting

VCasT can process output from external tools like the Model Evaluation Tools (MET), making it easy to integrate into existing verification workflows.

Supported Formats
-----------------

VCasT supports input from common meteorological and machine learning data formats, including:

- **GRIB2**: Standard in operational weather modeling
- **NetCDF**: Widely used in research and model development
- **Zarr**: Optimized for cloud and AI workflows, commonly used with ML-based weather models

Why Use VCasT?
--------------

- **Focused**: Built specifically for weather forecast verification
- **Lightweight**: YAML-driven configuration with no required boilerplate code
- **Flexible**: Easily integrated into larger Python-based workflows
- **Transparent**: Encourages reproducible, configurable, and interpretable analysis

Use Cases
---------

VCasT supports workflows such as:

- Validating new weather model configurations
- Comparing multiple ensemble or deterministic forecasts
- Generating verification summaries for operational systems
- Evaluating forecast skill across spatial domains and thresholds

Getting Started
---------------

To begin using VCasT, follow the  
:doc:`Quick Start Guide <../overview/quick-start>`