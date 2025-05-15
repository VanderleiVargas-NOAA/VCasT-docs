MET Stat Use Case: Fractions Skill Score (FSS)
==============================================

This use case demonstrates how to run VCasT to compute the Fractions Skill Score (FSS) using MET `.stat` files and a YAML configuration.

It uses a sample configuration file (`NBRCNT.yaml`) designed to evaluate neighborhood-based categorical skill metrics.

Prerequisites
-------------

Before running the example, make sure VCasT is installed. Follow the installation steps in  
:doc:`Quick Start Guide <../overview/quick-start>`.

Run the Example
---------------

1. **Clone the test repository:**

   .. code-block:: bash

      git clone https://github.com/NOAA-GSL/VCasT-tests
      cd VCasT-tests/examples/MET/fss

2. **Run VCasT with the provided YAML file:**

   .. code-block:: bash

      vcast NBRCNT.yaml

   This will load and process the `.stat` files under the `./stats` directory using the configuration options defined below.

YAML Configuration Explained
----------------------------

Below is the content of `NBRCNT.yaml`, which configures VCasT to:

- Use the NBRCNT line type for FSS
- Focus on REFC forecasts
- Filter by model, variable, threshold, lead time, and region.
- Aggregate results by model and lead time

.. literalinclude:: ../../_static/cfg_examples/fss.yaml
   :language: yaml
   :caption: Sample NBRCNT.yaml configuration
   :linenos:

Output
------

Three outputs are expected:
- ``filtered_output.data`` - File containing all the information filtered from MET stat files, including all the columns associated with nbrcnt line type.
- ``vars.data`` - File containing all the information filtered from MET stat files with only the specific ``stat_vars`` columns.
- ``agg.data`` - File containing the aggregated result.