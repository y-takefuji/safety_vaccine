# safety_vaccine 
[![Open in Code Ocean](https://codeocean.com/codeocean-assets/badge/open-in-code-ocean.svg)](https://codeocean.com/capsule/7deeac37-cbb7-4969-ad30-dcb2f423fc47/tree)

DOI: https://doi.org/10.24433/CO.6387836.v1

Takefuji Y. Set Operations in Python for Translational Medicine. International Journal of Translational Medicine. 2022; 2(2):174-185. 
https://doi.org/10.3390/ijtm2020015 

The latest data of VAERS (Vaccine Adverse Event Reporting System) dataset is 
available at:

https://vaers.hhs.gov/eSubDownload/index.jsp?fn=2021VAERSData.zip

effectiveness of vaccination status

https://data.cdc.gov/api/views/3rge-nu2a/rows.csv?accessType=DOWNLOAD

vuv.py is for calculating vaccine effectiveness on mortality between fully vaccinated and unvaccinated.

vuc.py is for calculating vaccine effectiveness on infection between fully vaccinated and unvaccinated.

vuc3.py is for calculating vaccine effectiveness on infection and death between fully vaccinated and unvaccinated by vaccine product.

vuc4.py is for calculating bivalent vaccine effectiveness on infection between fully vaccinated and unvaccinated by age group.

# set operations
vaers.py shows a good example of intersection operation. 

set(A).intersection(B)

set(A).symmetric_difference(B)

set(A).difference(B)

set(A).union(B)
<pre>
 set([1,2,5]).symmetric_difference([1,2,9,4,8,9])
 {4, 5, 8, 9}
 
 set([1,2,5]).difference([1,2,9,4,8,9])
 {5}
 
 set([1,2,5]).intersection([1,2,9,4,8,9])
 {1, 2}
 
 set([1,2,5]).union([1,2,9,4,8,9])
 {1, 2, 4, 5, 8, 9}
</pre>
The following figure shows what is intersection operation.

<img src="https://github.com/y-takefuji/safety_vaccine/raw/main/set.jpg" width=700 height=560 >

# How to install vaers
On WSL on Windows, MacOS, or Linux operating systems:

$ pip install vaers

On Windows 11 or 10:

$ pip install vaers --force-reinstall --no-cache-dir --no-binary :all:

# How to run vaers
$ vaers

or

$ vaers 2022


# How to run vaers.py

<pre>
0. Download 2021VAERSData.zip
1. Unzip 2021VAERSData.zip file
2. Run vaers.py program
$ python vaers.py
total instances:  677514
total deaths 8926
NOVIDs instances:  1202
NOVIDs deaths:  4
NOV death per instance 0.003328
MODERNA+PFIZER: 905
MODERNA+PFIZER death: 4
MODERNA+PFIZER death per instance: 0.00442
MODERNAIDs instances:  299195
MODERNA deaths 3648
MODERNA 0.012193
PFIZERIDs instances:  283061
PFIZER deaths 3969
PFIZER 0.014022
</pre>
# How to run pfizerAge.py to generate a pfizer.csv file.
<pre>
$ python pfizerAge.py
</pre>

# How to run modernaAge.py to generate a moderna.csv file.
<pre>
$ python modernaAge.py
</pre>

# How to calculate safety thresholds of PFIZER and MODERNA vaccines by age
<pre>
$ python deathperinstance.py
</pre>

# Subtraction operation

set(A).difference(B)

# Union operation

set(A).union(B)

# Symmetric difference (ExclusiveOR)

set(A).symmetric_difference(B)

