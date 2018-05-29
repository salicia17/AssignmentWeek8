# AssignmentWeek8viaCodepath/Facebook
# Project 8 - Pentesting Live Targets

Time spent: 13 to 15 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection: Open up a browser to https://35.226.34.105/blue/public/territories.php. Select the salesperson page to conduct the exploit. The exploit will be conducted via the URL. Using the given statement, ' OR SLEEP(5)=0--'. The SQL statement will produce a blind SQL injection. Put given statement after the https://35.226.34.105/blue/public/salesperson.php?id=1' OR SLEEP(5)=0--'. This will load the page for a few seconds, but then it returns back to the page.

Vulnerability #2: Session Hijacking: Open up a browser to https://35.226.34.105/blue/public/territories.php. The exploit will be done via the tool provided by "public/hacktools/change_session_id.php" and two browsers will be use. Open the Firefox browser and go to the sessiond_id.php page. Google browser will be already open. Copy the sessionId and paste the sessionId in the Firebox browser. Load the page with the new sessionId in Firebox browser. In the https://35.226.34.105/blue/public/territories.php, go to the login page. You will be automatically login without the need of credentials. 


## Green

Vulnerability #1: User Enumeration: 

Vulnerability #2: Cross Site Scripting: Open up a brower to https://35.226.34.105/green/public/territories.php. Go to the Contact Us form page where the exploit will be conducted. 


## Red

Vulnerability #1: 

Vulnerability #2: 


## Notes
