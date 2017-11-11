<h3 align="center">
  <img src="https://user-images.githubusercontent.com/4778878/30754005-b7a7e808-9f86-11e7-8b0f-79d1006babdf.jpg" alt="fastlane Logo" />
</h3>

# DVH Analytics
<img src='https://user-images.githubusercontent.com/4778878/30643873-2115f6de-9dd6-11e7-9d6c-c51dd8307384.jpg' align='right' width='300' alt="DVH Analytics screenshot">  
 
DVH Analytics is a software application to help radiation oncology departments build an in-house database of treatment planning data 
for the purpose of historical comparisons and statistical analysis. This code is still in development.  Please contact the developer if  you are interested in testing or collaborating.

The application builds a SQL database of DVHs and various planning parameters from DICOM files 
(i.e., Plan, Structure, Dose). Since the data is extracted directly from DICOM files, we intend
to accommodate an array of treatment planning system vendors.

In addition to viewing DVH data, this software provides methods to:

- download queried data
- view plan contours
- create time-series plots of various planning and dosimetric variables
- calculate correlations
- and generate multi-variable linear regressions.


The code is built upon these core libraries:
* [pydicom](http://code.google.com/p/pydicom/) - Read, modify and write DICOM files with python code
* [dicompyler-core](https://pypi.python.org/pypi/dicompyler-core) - Extensible radiation therapy research platform and viewer for DICOM and DICOM RT
* [Bokeh](http://bokeh.pydata.org/en/latest/index.html) - Interactive Web Plotting for Python

For installation instructions, see our [installation notes](https://github.com/cutright/DVH-Analytics/blob/master/install_notes.md).

This application was presented at the AAPM Midwest Chapter 2017 Fall meetings. The slides are available [here](https://www.dropbox.com/s/gtaxd5dp69508cu/DVH%20Analytics.mp4?dl=0).

## Dependencies
* [Python](https://www.python.org) 2.7  
    * Python 3 not currently supported
    * [Future](https://pypi.python.org/pypi/future) 0.16.0
        * for bridging gap between 2.7 and 3.x
        * we're still working on the Python 3 transition for DVH Analytics
* [PostgreSQL](https://www.postgresql.org/) and [psycopg2](http://initd.org/psycopg/)
* [SciPy](https://scipy.org)
    * [NumPy](https://pypi.python.org/pypi/numpy) 1.12.1 tested
* [pydicom](https://github.com/darcymason/pydicom) 0.9.9
* [shapely](https://github.com/Toblerity/Shapely) 1.6b2
* [fuzzy wuzzy](https://github.com/seatgeek/fuzzywuzzy) 0.15
* [Statsmodels](https://github.com/statsmodels/statsmodels) 0.8.0
* [dicompyler-core](https://pypi.python.org/pypi/dicompyler-core) 0.5.3
    * requirements per [developer](https://github.com/bastula)
        * [numpy](http://www.numpy.org/) 1.2 or higher
        * [pydicom](https://github.com/pydicom/pydicom) 0.9.9 or higher
            * pydicom 1.0 is preferred and can be installed via pip using: pip install https://github.com/darcymason/pydicom/archive/master.zip
        * [matplotlib](http://matplotlib.sourceforge.net/) 1.3.0 or higher (for DVH calculation)
        * [six](https://pythonhosted.org/six/) 1.5 or higher
* [Bokeh](http://bokeh.pydata.org/en/latest/index.html) 0.12.10
    * requirements per [developer](http://bokeh.pydata.org/en/latest/docs/installation.html)
        * [NumPy](http://www.numpy.org/)
        * [Jinja2](http://jinja.pocoo.org/)
        * [Six](https://pythonhosted.org/six/)
        * [Requests](http://docs.python-requests.org/en/master/user/install/)
        * [Tornado](http://www.tornadoweb.org/en/stable/) >= 4.0, <=4.4.2
        * [PyYaml](https://pypi.python.org/pypi/pyaml)
        * [DateUtil](https://pypi.python.org/pypi/python-dateutil)
