MET Stat Use Case: Performance Diagram
======================================

This use case demonstrates how to run VCasT to compute categorical statistics for performance diagrams using MET `.stat` files and a YAML configuration.

It uses a sample configuration file (`cts.yaml`) tailored to produce POD, Success Ratio, and other skill metrics for plotting.

Prerequisites
-------------

Before running the example, make sure VCasT is installed. Follow the installation steps in  
:doc:`Quick Start Guide <../overview/quick-start>`.

Run the Example
---------------

1. **Clone the test repository:**

   .. code-block:: bash

      git clone https://github.com/NOAA-GSL/VCasT-tests
      cd VCasT-tests/examples/MET/performance_diagram

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

.. literalinclude:: ../../_static/cfg_examples/performance_diagram.yaml
   :language: yaml
   :caption: Sample cts.yaml configuration
   :linenos:

Output
------

An aggregated result will be saved to:

- ``APCP01_agg.data`` -  Categorical statistics for performance diagram generation.
