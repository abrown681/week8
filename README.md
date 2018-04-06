# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

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

Vulnerability #1: SQL Injection (SQLi)
- To replicate: go to the public salesperson search page. Click on a salesperson's link. Replace their id number in the url with "' OR SLEEP(5)=0--'". Once you redirect to this new URL, the current page will remain open and you will not get a "person not found" error.
- GIF walkthrough: https://github.com/abrown681/week8/blob/master/SQL%20Injection%20(SQLi).gif

Vulnerability #2: __________________


## Green

Vulnerability #1: Username Enumeration
- To replicate: if you go to log in as a user that exists in the database and input the wrong password, the "log in was unsuccessful message" will be bolded revealing that a user with that name exists. If the username doesn't exist in the database, the message will not be bolded.
- GIF walkthrough: https://github.com/abrown681/week8/blob/master/Username_Enumeration.gif

Vulnerability #2: Cross-Site Scripting (XSS)
- To replicate: go to the public comments page. As "testuser" with "test@testemail.com" type in the following comment: `<script>alert('testing alert')</script>`. When you access the comments page as an admin, an alert saying "testing alert" will popup.
- GIF walkthrough: https://github.com/abrown681/week8/blob/master/Cross-Site%20Scripting%20(XSS).gif


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
- To replicate: go to the public salesperson search page. Click on a salesperson's link. In the url, replace the id number with either 10 or 11 and you will be directed to user pages that reveal information about hidden users.
- GIF walkthrough: https://github.com/abrown681/week8/blob/master/Insecure%20Direct%20Object%20Reference%20(IDOR).gif

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work
