MET Stat Use Case: Spread–Skill Relationship
============================================

This use case demonstrates how to run VCasT to evaluate the spread–skill relationship using MET `.stat` files and an ensemble continuous statistics configuration.

It uses a sample configuration file (`ecnt.yaml`) for computing metrics like CRPS and ensemble spread.

Prerequisites
-------------

Before running the example, make sure VCasT is installed. Follow the installation steps in  
:doc:`Quick Start Guide <../overview/quick-start>`.

Run the Example
---------------

1. **Clone the test repository:**

   .. code-block:: bash

      git clone https://github.com/NOAA-GSL/VCasT-tests
      cd VCasT-tests/examples/MET/spread-skill

2. **Run VCasT with the provided YAML file:**

   .. code-block:: bash

      vcast ecnt.yaml

   This will load and process ensemble `.stat` files under the `./estats` directory using the configuration options defined below.

YAML Configuration Explained
----------------------------

Below is the content of `ecnt.yaml`, which configures VCasT to:

- Use the `ecnt` line type for ensemble continuous verification
- Filter by model, variable, threshold, lead time, and region
- Aggregate the results by model, variable, and lead time

.. literalinclude:: ../../_static/cfg_examples/spread_skill.yaml
   :language: yaml
   :caption: Sample ecnt.yaml configuration
   :linenos:

Output
------

There are two output files:

- ``vars.data`` - File containing all the information filtered from MET stat files with only the specific ``stat_vars`` columns.
- ``agg.data`` — Aggregated reliability metrics.

.. note::
   The option ``stat_vars: ["ratio"]`` means that ``ratio = spread_plus_oerr / rmse`` is also calculated.