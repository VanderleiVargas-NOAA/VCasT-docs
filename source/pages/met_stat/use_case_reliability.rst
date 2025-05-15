MET Stat Use Case: Reliability Diagram
======================================

This use case demonstrates how to run VCasT to compute probabilistic metrics used for reliability diagrams using MET `.stat` files and a YAML configuration.

It uses a sample configuration file (`pct.yaml`) that filters and aggregates probabilistic forecast statistics.

Prerequisites
-------------

Before running the example, make sure VCasT is installed. Follow the installation steps in  
:doc:`Quick Start Guide <../overview/quick-start>`.

Run the Example
---------------

1. **Clone the test repository:**

   .. code-block:: bash

      git clone https://github.com/NOAA-GSL/VCasT-tests
      cd VCasT-tests/examples/MET/reliability

2. **Run VCasT with the provided YAML file:**

   .. code-block:: bash

      vcast pct.yaml

   This will load and process the probabilistic `.stat` files under the `./stats` directory using the configuration options defined below.

YAML Configuration Explained
----------------------------

Below is the content of `pct.yaml`, which configures VCasT to:

- Use the `pct` line type for probabilistic verification
- Filter by model, variable, threshold, lead time, and region
- Aggregate the results by model, variable, and lead time

.. literalinclude:: ../../_static/cfg_examples/reliability.yaml
   :language: yaml
   :caption: Sample pct.yaml configuration
   :linenos:

Output
------

There are two output files:

- ``vars.data`` - File containing all the information filtered from MET stat files with only the specific ``stat_vars`` columns.
- ``agg.data`` — Aggregated reliability metrics.

.. note::
   The option ``stat_vars: ["all_thresh"]`` means that all thresholds will be used. See Table 11.8 in `MET Point-Stat tool <https://metplus.readthedocs.io/projects/met/en/latest/Users_Guide/point-stat.html>` 