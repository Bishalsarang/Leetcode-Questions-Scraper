# Leetcode Questions Scrapper

Leetcode Questions Scrapper is a simple scrapper built on top of Selenium that fetches all the problems from leetcode and write as html and epub files.

You can download the sample html and epub containing 11  problems [here](https://github.com/sarangbishal/Leetcode-Questions-Scrapper/tree/master/assets/sample%20output%20files).

## Requirements
	
I have tested it on windows machine running with Google Chrome 77.0.3865.75 and chrome driver from [here](https://chromedriver.storage.googleapis.com/index.html?path=77.0.3865.40/) and put it inside driver directory.
I haven't tested with Linux and Mac but you can download chrome driver for respective platform and make change to `CHROMEDRIVER_PATH`   inside `main.py`

Pip install all the requirements.

    requests==2.22.0
    beautifulsoup4==4.8.0
    selenium==3.141.0
    EbookLib==0.17.1

    
## How to use
 - Clone the repo and install all the dependencies including latest google chrome and latest chrome driver
 - Update chrome driver path 
 - Run the following commands to download all algorithmic problems from leetcode
 `python main.py`
 ![enter image description here](https://raw.githubusercontent.com/sarangbishal/Leetcode-Questions-Scrapper/master/assets/screenshots/main.PNG?token=AG2ULFBE5HCEDG2FYTXPFW25RNWCU)
 <br>This downloads problem contents to 2 files: *****out.html***** and ***chapters.pickle***.

 **NOTE:** Leetcode may temporarily block requests. If the error occurs, wait for sometime and try again or use the proxy. Don't worry, Since, the previous state is saved to ***track.conf*** file, the download resumes from where it failed.
 
 Here is how sample ***out.html*** looks like.
 ![Sample out.html](https://raw.githubusercontent.com/sarangbishal/Leetcode-Questions-Scrapper/master/assets/screenshots/sample_out_html.PNG?token=AG2ULFBT3PWYY2VZZYDUEES5RNVBI)
 
 After ***main.py*** script executes successfully. The pickle file is automatically converted to "***Leetcode Questions.epub***". 
 
 But you can also convert manually to epub with existing downloaded content with.
 `python epub_writer.py`
 ![enter image description here](https://raw.githubusercontent.com/sarangbishal/Leetcode-Questions-Scrapper/master/assets/screenshots/epub_writer.PNG?token=AG2ULFC6Q63GEO6JOK6FH4C5RN26O)
 
 Here is how sample epub file looks like
![Sample](https://raw.githubusercontent.com/sarangbishal/Leetcode-Questions-Scrapper/master/assets/screenshots/sample_out_epub.PNG?token=AG2ULFBGUDY5D4FCJ7SENZK5RNVFQ)

You can download sample files from here which contains 11 problem.
1. [Sample Out.epub](https://github.com/sarangbishal/Leetcode-Questions-Scrapper/blob/master/assets/sample%20output%20files/out.epub)
2. [Sample Out.html](https://github.com/sarangbishal/Leetcode-Questions-Scrapper/blob/master/assets/sample%20output%20files/out.htmlhttps://github.com/sarangbishal/Leetcode-Questions-Scrapper/blob/master/assets/sample%20output%20files/out.html)

