VCasT Documentation
===================

Quick Start Guide
-----------------

**1. Create a virtual environment**

.. code-block:: bash

   python -m venv venv

**2. Activate the environment**

.. code-block:: bash

   source venv/bin/activate

**3. Install VCasT from GitHub**

Full version (recommended):

.. code-block:: bash

   pip install "git+https://github.com/NOAA-GSL/VCasT.git@develop#egg=vcast[all]"

Lite version:

.. code-block:: bash

   pip install "git+https://github.com/NOAA-GSL/VCasT.git@develop#egg=vcast[lite]"

**4. Confirm the installation**

.. code-block:: bash

   which vcast

**5. Clone test suite**

.. code-block:: bash

   git clone https://github.com/NOAA-GSL/VCasT-tests
   mv VCasT-tests tests

**6. Install pytest and run tests**

.. code-block:: bash

   pip install pytest
   pytest -v tests

**7. (Optional) Clone VCasT with submodules**

.. code-block:: bash

   git clone https://github.com/NOAA-GSL/VCasT
   cd VCasT
   git submodule update --init --recursive


.. toctree::
   :maxdepth: 2
   :caption: Contents:
