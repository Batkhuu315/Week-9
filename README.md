# Week 9 - Pentesting Live Targets

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

Vulnerability #1: __SQL Injection___

Vulnerability #2: __Session Hijacking/Fixation__

# SQL Injection

![](picture/Blue1.1.png)

i was tried to input single quotation mark into URL, and it gives me error which means it is not sanitized. So i tried bunch of different SQL query and find this one : ' or '1 = 1'--'   

![](picture/Blue1.2.png)

![](picture/Blue1.3.png)


# Session Hijacking/Fixation

First i was logged in as a admin in my chrome web browser and got session id while using "public/hacktools/change_session_id.php". 

![](picture/Blue2.1.png)

After that i checked regular users session id using safari web browser and it different 

![](picture/Blue2.2.png)

Changed regular users session id to log in as admin

![](picture/Blue2.3.png)

![](picture/Blue2.4.png)

## Green

Vulnerability #1: __Cross-Site Scripting__

Vulnerability #2: __Username Enumeration__


# Cross-Site Scripting

Leaved contained XSS feedback on Feedback section. 
When admin checked Feedback section it will trigerred.

![](picture/Green1.1.png)

![](picture/Green1.2.png)

# Username Enumeration

When im trying to log in random username and password it gives me message says "Log in was unsuccessful".

![](picture/Green2.1.png)

If i trying to log in correct username but random password it gives same message as "Log in was unsuccessful" but this time error message displayed different color from random username.

![](picture/Green2.2.png)

## Red

Vulnerability #1: __Insecure Direct Object Refence__

Vulnerability #2: __Cross-Site Reguest Forgery__

# Insecure Direct Object Refence

Checked Salesperson page and tried to editing URL's id value and found IDOR vulnerability.
This is public access page 

![](picture/Red1.1.png)

Those are restricted access pages

![](picture/Red1.2.png)

![](picture/Red1.3.png)

![](picture/Red1.4.png)

# Cross-Site Reguest Forgery

All other vulerabilities found except CSRF so i thought it belongs here. i was trying to upload malicious feedback section and wait to admin click it and its trigerred to changing user name but i couldn't figured out how to do it or my written code does not work. 

![](pic/Red 2.1.png)

![](pic/Red 2.2.png)

![](pic/Red 2.3.png)

![](pic/Red 2.4.png)

Plus only red page loads without error when im changing "csrf_token value"

![](pic/Red 2.5.png)


## Notes

Describe any challenges encountered while doing the work

Tried to download and use LICEcap but it was not work properly.
So i uploaded pictures instead of GIF file.
