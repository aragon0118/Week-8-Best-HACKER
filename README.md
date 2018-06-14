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

Vulnerability #2: Cross-Site Request Forgery (CSRF)
![](https://github.com/aragon0118/Week-8-Best-HACKER/blob/master/CSRF%20Week%208.gif)



## Concept Review

**Which attacks were easiest to execute? Which were the most difficult?
User enumeration was the easiest because of the method I determined the vulnerability. The Cross-site Request Forgery was the very difficult for me.
What is a good rule of thumb which would prevent accidentally username enumeration vulnerabilities like the one created here?**

*The website should never display if a user exits! This error includes not only the message returned to the user, but changes to the page contents (HTML, CSS, images, form structure or values), URL, or even cookie data.*

**Many SQL Injections use OR as part of the injected code. (For example: ' OR 1=1 --'.) Could AND work just as well in place of OR? (For example: ' AND 1=1 --'.) Why or why not?**

*The difference between “AND” and “OR” in SQL is that AND is for all conditions separated are true and OR any conditions separated are true.*

**Imagine that one of your classmates is an authorized admin for the site's CMS and you are not. How would you get them to visit the self-submitting, hidden page you created in Objective #5 (CSRF)?**

*With a little social engineering I would send my classmate a private message containing a link they might fall for.*

**Compare session hijacking and session fixation. Which attack do you think is easier for an attacker to execute? Why? One of them is much easier to defend against the other. Which one and why?**

*There is not much a big difference session hijacking and session fixation. When someone uses session hijacking it is to gain access to a session of another user by trying to get the ID of a victim’s session to use their session. Unlike session fixation, the attacker already has access to a valid session and tries to force the victim to use this particular session.*


