Requirements
------------
* Removed pvlib version restrictions in setup.py. Previously "pvlib >= 0.11.0, <0.12.0", now "pvlib".
* Updated pvlib version in requirements.txt from 0.11.0 to 0.13.1
* Added pandas upper version restriction in setup.py. Now "pandas >= 1.4.4, <3.0.0".
* Added numpy upper version restriction in setup.py. Now "numpy >= 1.22.4, <2.3.0".
* Updated pandas version in requirements.txt from 2.2.2 to 2.2.3 for python 3.13 compativility.
* Updated scipy version in requirements.txt from 1.13.1 to 1.14.1 for python 3.13 compatibility.
* Updated h5py version in requirements.txt from 3.11.0 to 3.12.0 for python 3.13 compatibility.
* Updated scikit-learn version in requirements.txt from 1.5.1 to 1.6.0 for python 3.13 compatibility.
* Updated plotly version in requirements.txt from 5.23.0 to 6.1.1 for python 3.13 compatibility.
* Updated setuptools-scm version in requirements.txt from 8.1.0 to 9.2.2 for python 3.13 compatibility.


Warnings
--------
* Added filter to ignore deprecation warning related to IPyNbFile in setup.cfg.