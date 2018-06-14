# Project 8 - Pentesting Live Targets

Time spent: **12** hours spent in total

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

Vulnerability #1: Session Hijacking/Fixation: I inserted the script given by codepath and changed the session ID.
```
public/hacktools/change_session_id.php
```
![](https://github.com/aragon0118/Week-8-Best-HACKER/blob/master/Session%20Hijacking%20Week%208.gif)

Vulnerability #2: SQL Injection: I used the hint (blind ejection example) give by codepath.
```
' OR SLEEP(5)=0--' 
```
![](https://github.com/aragon0118/Week-8-Best-HACKER/blob/master/SQL%20Week%208.gif)


## Green

Vulnerability #1: Username Enumeration: I used the existing username given by codepath.
```
username "jmonroe99"
```
![](https://github.com/aragon0118/Week-8-Best-HACKER/blob/master/Username%20Enumeration%20Week%208.gif)

Vulnerability #2: Cross-Site Scripting (XSS): I used the script provided by codepath.
```
<script>alert('Mallory found the XSS!');</script>
```
![](https://github.com/aragon0118/Week-8-Best-HACKER/blob/master/XSS%20Week%208.gif)

## Red

Vulnerability #1: Insecure Direct Object Refernce (IDOR):The red site returned sensitive information after ID=9.

![](https://github.com/aragon0118/Week-8-Best-HACKER/blob/master/IDOR%20Week%208.gif)

Vulnerability #2: Cross-Site Request Forgery (CSRF):



## Notes

Describe any challenges encountered while doing the work
