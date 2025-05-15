MET Stat Use Case: Categorical Scores
=====================================

This use case demonstrates how to run VCasT to compute categorical statistics using MET `.stat` files and a YAML configuration.

It uses a sample configuration file (`cts.yaml`) that filters and aggregates categorical scores like POD, FAR, CSI, FBIAS, and GSS for reflectivity forecasts.

Prerequisites
-------------

Before running the example, make sure VCasT is installed. Follow the installation steps in  
:doc:`Quick Start Guide <../overview/quick-start>`.

Run the Example
---------------

1. **Clone the test repository:**

   .. code-block:: bash

      git clone https://github.com/NOAA-GSL/VCasT-tests
      cd VCasT-tests/examples/MET/cts_metrics

2. **Run VCasT with the provided YAML file:**

   .. code-block:: bash

      vcast cts.yaml

   This will load and process the `.stat` files under the `./stats` directory using the configuration options defined below.

YAML Configuration Explained
----------------------------

Below is the content of `cts.yaml`, which configures VCasT to:

- Load categorical statistics (``line_type: cts``)
- Filter by model, variable, threshold, lead time, and region
- Aggregate the results by model, variable, and lead time

.. literalinclude:: ../../_static/cfg_examples/cts.yaml
   :language: yaml
   :caption: Sample cts.yaml configuration
   :linenos:

Output
------

Since both `reformat_file` and `output_file` are set to `false`, the only output in this example will be an aggregated result saved to ``REFC_agg.data``.

You can modify the YAML to enable full data dumps as needed.

