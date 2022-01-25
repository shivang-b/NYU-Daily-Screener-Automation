# NYU-Daily-Screener-Automation

### Daily Screener
To enter NYU facilities, all NYU community members must fill out a form (available on the NYU Mobile app and on their website) and authenicate their account with single sign-on (SSO) (including getting through DUO security). Individuals must receive a green PASS to be permitted, whereas a red FAIL restricts access. The system sends a green PASS automatically if NYU has no record of the individual being infected by COVID-19 (NYU could be informed by a postive result on a PCR test, which individuals don't take daily) or the individual has not met NYU's vaccine policy (unless they receive exemption).

### Motivation
Although the NYU Daily Screener attempts to prevent the NYU Community from being harmed by the COVID-19 pandemic, NYU Community members must daily log in to their NYU Mobile app to get the green PASS. The problem is the repetitive, monotonous task of completing the form, even though it takes under 5 minutes of one's time. I hope to automate this process.

### Target audience
Since the code requires python installation, use of selenium, and a webdriver (all without much GUI), this code is aimed at people familiar with Python programming (even if you have only taken the introductory programming course). Even if you have no experience with selenium, you'll be good to go.

### Downloading and Installing
Even though I use Brave, I ran my code on Edge because I was having issues with the correct webdriver. You can download Microsoft Edge here: 'https://www.microsoft.com/en-us/edge'
Search 'edge://settings/help' on Edge, ensure you are up-to-date, and note down the Version.
Head over to 'https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/' and download the webdriver. I recommend installing the x86 version, even if your computer is 64-bit because that's the one which worked for me. Extract the compressed folder and note down the path to the webdriver.
On command prompt, run the following: 'pip install msedge-selenium-tools selenium==3.141'

### Python code
In the Daily Screener Automation.ipynb file (which I recommend you run in Jupyter Notebooks, as did I), replace the 'WEBDRIVER PATH' with the webdriver path noted previously and insert your NYU Net ID and password in the appropriate fields; keep in mind to retain the double/single quotes but to replace the uppercase words and the brackets.

### Run it
I recommend commenting the '--headless' line to ensure the code actually works correctly.
Next, assuming you use Jupyter Notebooks, paste the code in a Jupyter Notebook and run all the code except the last block that says 'driver.quit()'. Upon completion of that code, you will receive a DUO security push to authenticate that request.

### Improvements
A massive improvement would be if someone can figure out how to use the requests package with the Daily Screener because then we could run the program from our smartphones, the end-user would not have to go through this technicality, and could get the PASS with the tap of a button.
