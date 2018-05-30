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

Vulnerability #1: User Enumeration: Open up a browser to https://35.226.34.105/green/public/territories.php. There is a username enumeration vulnerability. Keep in mind that when login as admin, you realize there are only three users. Go to the Login page and begin typing different usernames. Type in "jmonroe99"and we can that the user exists. A bold error is shown. An invalid user shows an unbolded error. This vulnerability allows you to determine valid user accounts. 

Vulnerability #2: Cross Site Scripting: Open up a brower to https://35.226.34.105/green/public/territories.php. Go to the Contact Us form page where the exploit will be conducted. Fill out the form by inputting information on the fill text boxs. In the feedback text box, place <script>alert('putyournamehere found the XSS!');</script> and submit. Login as admin to view the feedback and go to the Feedback section and the XSS is executed. 


## Red

Vulnerability #1: IDOR: Open up a browser to https://35.226.34.105/red/public/territories.php. You can go to the Salesperson tab on the website. You will be able to change the parameter ID in the URL. We can find different salespeople.ID's with 10 and 11 shouldn't be accessible by everyone. The other two websites won't allow you to see this information.

Vulnerability #2: CSRF: Open up a browser to https://35.226.34.105/red/public/territories.php. You will go to the User list tab so see all users. Click on the edit tab for the user to edit user information. Open the Inspect element on Google Chrome developer tools. Go to form and change the CSRF token. Change user information such as user name. Submit new changes. Changes were made successfully without getting an invalid equest such as the other BLUE and Green websites. 


## Notes
