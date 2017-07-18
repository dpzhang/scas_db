# SCAS Database Scraper Mannual
Author: Dongping 'Gabriel' Zhang

Email: dpzhang@uchicago.edu

## About this repository:
This repository contains the user manual of SCAS Database scraper written by 
[Gabriel Zhang](https://github.com/dpzhang) for __Compass Lexecon__. 
The scrapper is completely written in Python 3.6. 

## Disclaimer
Due to confidentiality, code would not be published or released from this 
repository, and this manual is written soly for __Compass Lexecon__ staff who 
will be using the scraper.

## Preparation 

### Step 1: Install Cygwin
* Download __Cygwin__ from [here](https://cygwin.com/install.html) by left-clicking __setup-x86\_64.exe__ once get to the page.
__Suggestion:__ I would recommend users to save this installation file on the Desktop in case some other packages or softwares are needed in the future.

* Procedures to install __Cygwin__:
    + Keep clicking __Next__ button until __Select Packages__.
    + Click on the dropdown list of __View__, and then select __Full__ option.
    + In __Search__, type in <code>Python3</code> and wait for the list 
to update.
    + Four packages are needed and they are listed below. For each of those packages, click on __Skip__ under 
the __New__ column, and select the newest version to install.
        - <code>python3-devel: Py3K language interpreter</code> 
        - <code>python3-ipython: Interactive Python interpreter</code>
        - <code>python3-pip: Python package installation tool</code>
        - <code>python3-zmq: Python 0MQ bindings</code>
    + Keep clicking __Next__ to finish installation.


### Step 2: Install Packages
* Open __Cygwin__, and type in the following command.
```bash
pip3 install selenium openpyxl
```
__Notice:__ You only need to install required packages once in a machine.

## How to use scraper:

