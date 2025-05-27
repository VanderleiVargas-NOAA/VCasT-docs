VCasT Plotting YAML Configuration
=================================

This page describes the structure and fields of the YAML file used to configure the **Plotting** module in VCasT. This file controls how statistical outputs (from `.stat` files or pre-processed CSVs) are visualized through line plots and aggregated summaries.

Example YAML File
-----------------

.. literalinclude:: ../../_static/cfg_examples/plot_config.yaml
   :language: yaml
   :caption: Sample Plotting Configuration YAML

Configuration Sections
----------------------

The YAML file is divided into several sections:

Input Data Settings
^^^^^^^^^^^^^^^^^^^

- **input_file**:  
  Path to the CSV file containing extracted or aggregated statistics to plot. This file should include all relevant columns required by the plot type (e.g., model, stat_name, fcst_lead, value, etc.).

Plot Settings
^^^^^^^^^^^^^

- **x_axis**:  
  Column to use as the x-axis (e.g., `fcst_lead`, `threshold`, `vx_mask`).

- **y_axis**:  
  Column containing the metric values to plot (e.g., `value`, `mean`).

- **series_by**:  
  Column to group different lines/series on the same plot (e.g., `model`, `fcst_var`).

- **split_by**:  
  (Optional) Column to split plots into multiple subfigures. One plot per unique value (e.g., `stat_name`, `vx_mask`).

- **stat_filter**:  
  List of statistical metrics to include (e.g., `[fbias, gss, csi]`). Used when input includes multiple metrics.

Output and Style Options
^^^^^^^^^^^^^^^^^^^^^^^^

- **title**:  
  Custom plot title. If omitted, a default title based on variables and settings is generated.

- **x_label** / **y_label**:  
  Labels for the x and y axes. Optional; defaults are derived from the column names.

- **output_file**:  
  Path to save the resulting plot. Recommended extensions are `.png`, `.pdf`, or `.svg`.

- **dpi**:  
  Image resolution in dots per inch (e.g., `150`, `300`).

- **show_significance**:  
  [`true`, `false`] whether to visually mark statistically significant results (requires significance column in the data).

Additional Options
^^^^^^^^^^^^^^^^^^

- **legend**:  
  [`true`, `false`] whether to display a legend on the plot.

- **y_lim**:  
  `[min, max]` range to constrain the y-axis.

- **x_lim**:  
  `[min, max]` range to constrain the x-axis (optional).

- **style**:  
  Plot style (e.g., `line`, `scatter`, `errorbar`). Determines the format used to draw series.

---

For examples of plotting configuration files and output images, see the `examples/plotting/` directory.
