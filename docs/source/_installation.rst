
First, make sure you have a python environment installed. We recommend miniconda3 or anaconda3.

.. code:: bash

    conda --version

Then from scratch create a virtual environment for pymoo:

.. code:: bash

    conda create -n pymoo -y python==3.6 cython numpy
    conda activate pymoo


For the current stable release please execute:

.. code:: bash

    pip install pymoo

For the current development version:

.. code:: bash

    git clone https://github.com/msu-coinlab/pymoo
    cd pymoo
    pip install .

Since for speedup some of the modules are also available compiled you can double check
if the compilation worked. When executing the command be sure not already being in the local pymoo
directory because otherwise not the in site-packages installed version will be used.

.. code:: bash

    python -c "from pymoo.cython.function_loader import is_compiled;print('Compiled Extensions: ', is_compiled())"

