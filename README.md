# SCAS Database Scraper \\User Mannual
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

### Step 1: Install Python for Windows
* Download __Python 3.x.x for Windows__ installation file from [here](https://www.python.org/downloads/]), 
the name of the installation file downloaded to your machine would typically look 
something like __python-3.x.x.exe__.
    + On July 25th, 2017, the newest version of __Python for Windows__ is version 3.6.2

* Double click the installation file to install Python
    + Check the box __''Add Python 3.6 to PATH''__.
    + Left-click __''Install now''__, and Python would be installed in designated location, such as <code>C:\Users\gzhang\AppData\Local\Programs\Python\Python36-32</code> in my machine.


### Step 2: Install Required Packages
* After downloading Python3, open a Windows Command Prompt. Copy and paste the 
command below and press enter. Windows will update all built-in package.
    + Reference [here](https://packaging.python.org/tutorials/installing-packages/)
    ```bash
    python -m pip install -U pip setuptools
    ```

* To install required pacakge, enter the following command to Windows Command 
Prompt. This command will install the latest version of a module and its 
dependencies from the Python Package Index.
    + Reference [here](https://docs.python.org/3/installing/index.html)
    ```bash
    python -m pip install selenium openpyxl
    ```

### Step 3: Download Chrome Browser and Chrome Driver
* Download Chrome browser [here](https://www.google.com/chrome/browser/).
* Download Chrome driver [here](https://sites.google.com/a/chromium.org/chromedriver/downloads).
    + Click on __Latest Release: ChromeDriver X.XX__
    + Download __chromedriver\_win32.zip__
    + Unzip the file to get __chromedriver.exe__
    + Drag and drop __chromedriver.exe__ to your Python3 home directory's subdirectory called Scripts.
        - For example, mine would be:
        ```bash
        C:\Users\gzhang\AppData\Local\Programs\Python\Python36-32\Scripts
        ```
        - Reference [here](https://github.com/SeleniumHQ/selenium-google-code-issue-archive/issues/2034)
        - ___Friendly reminder___: You only need to do this once in a machine.


## IV. SCAS DB Scraper
### __NOTICE__: in this manual, I assume the scraper file locates in <code>C:\Workdata\scas\_scraper.py</code>


* Determine __Start Filing Date__ and __End Filing Date__, and enter command 
below to Windows Command Prompt to run the scraper. 
    + For example, if you want to scrap all case profiles between 01/01/2016 
and 07/19/2017, use the following command.
        ```bash
        python C:\Workdata\scas_scraper.py 01/01/2016 07/19/2017
        ```
    + ___Friendly Reminder___: although the scraper is capable of scrapping data 
of any time interval from 1 day to 10 years or more, it is recommended to scrap 
case profiles within shorter time interval for faster job processing speed, and 
my recommendation would be 1 year. 

* When scrapping, a Chrome browser would be opened and the Windows Command Prompt 
instance will also inform you of the scrapping progress. Chrome browser would 
automatically maximize its window size by the program. So, if you do not 
want the browser to occupy your entire screen, you can minimize it to 
the task bar like most of windows programs. The current Chrome browser would 
likely to exit frequently and new browser windows would be initiated. This is 
normal and is caused by website auto-logout.


* __Notice: current official Chrome for Windows is in patch 59 which does not support 
headless mode (while MAC and Linux both does now). PhantomJS could be a solution but 
it is not as stable and reliable as Chrome. Thus for now I decide to stick to Chromedriver. 
When Google releases their patch 60 for Chrome, I will update the code accordingly.__
    + Reference [here](https://developers.google.com/web/updates/2017/04/headless-chrome)


## V. Check Scraped Files
* After scrapping completed successfully, go to <code>C:\Workdata</code>, and 
you will see a new directory called <code>case\_profiles</code>. Double-click 
to enter the directory, and you will see sub-directories in format of 
__MMDDYYYY-MMDDYYYY__ (For example, 01012016-07192017), and all scraped case 
profiles are stored in individual Excel format.
