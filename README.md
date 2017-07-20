# SCAS Database Scraper User Mannual
__Author__: Gabriel Zhang

__Email__: gzhang@compasslexecon.com

__Ext.__: 20639
## I. About this repository:
This repository contains the user manual of SCAS Database Scraper written by 
[Gabriel Zhang](https://github.com/dpzhang) for __Compass Lexecon__. 
The scraper is completely written in Python 3.6. 

## II. Disclaimer
Due to confidentiality, code would not be published or released from this 
repository, and this manual is written soley for __Compass Lexecon__ staffs who 
will be using the scraper.

## III. Preparation 

### Step 1: Install Cygwin
* Download __Cygwin__ from [here](https://cygwin.com/install.html) by left-clicking __setup-x86\_64.exe__ after getting to the page.
    + __Suggestion:__ I would recommend users to save this installation file on the Desktop in case some other packages or softwares are needed in the future.

* Procedures to install __Cygwin__:
    + Keep clicking on the __Next__ button until __Select Packages__.
    + Click on the dropdown list of __View__, and then select __Full__ option.
    + In __Search__, type in <code>Python3</code> and wait for the list 
to update.
    + After list got updated, four packages listed below would be needed to install. For each of those packages, click on __Skip__ under column __New__, and then select the newest version to install.
        - <code>python3-devel: Py3K language interpreter</code> 
        - <code>python3-ipython: Interactive Python interpreter</code>
        - <code>python3-pip: Python package installation tool</code>
        - <code>python3-zmq: Python 0MQ bindings</code>
    + Keep clicking __Next__ to finish installation.


### Step 2: Install Required Packages
* After downloading __Cygwin__, open __Cygwin__, and type in the following command.
    ```bash
    pip3 install selenium openpyxl
    ```
__Notice:__ You only need to install required packages once in a machine.


### Step 3: Download Chrome Browser and Chrome Driver
* Download Chrome browser [here](https://www.google.com/chrome/browser/)
* Download Chrome driver [here](https://sites.google.com/a/chromium.org/chromedriver/downloads)
    + Click on __Latest Release: ChromeDriver X.XX__
    + Download __chromedriver\_win32.zip__
    + Unzip the file to get __chromedriver.exe__
    + Drag and drop __chromedriver.exe__ to <code>C:\Windows\System32</code> directory

__Notice:__ You only need to install required packages once in a machine.

## IV. SCAS DB Scraper
### __NOTICE__: in this manual, I assume the scraper file locates in <code>C:\Workdata</code>

* Get to the directory that contains scraper by the following bash command.
    + You can copy and paste this command to __Cygwin__ bash prompt
        ```bash
        cd C:\Workdata\
        ```

* Determine __Start Filing Date__ and __End Filing Date__, and enter bash command 
below to run scraper. 
    + For example, if you want to scrap all case profiles between 01/01/2016 
and 07/19/2017, use the following command.
        ```bash
        python3 crawler.py '01/01/2016' '07/19/2017'
        ```

* When scrapping, a Chrome browser would be opened and the __Cygwin__ instance 
will also inform you of the scrapping progress. Chrome browser would 
automatically maximize its window size by the scraper program. If you do not 
want the browser to occupy your entire screen, you can minimize it to 
the task bar by clicking __``-''__ button on the top right cornor like most of 
windows programs. Typically every 40 mins, the current Chrome browser would 
exit and a new browser would be initiated. This is normal and is caused by 
website auto-logout.


* After scrapping, go to <code>C:\Workdata</code>, you will see a new directory 
called <code>case\_profiles</code>. Double-click to enter the directory, and you 
will see sub-directories in format of __MMDDYYYY-MMDDYYYY__ (For example, 
01012016-07192017), and all scraped case profiles are stored in individual
 Excel format.
