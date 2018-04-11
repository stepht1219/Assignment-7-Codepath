# Assignment-7-Codepath
Week 7 of Codepath Cybersecurity Course
# Project 7 - WordPress Pentesting

Time spent: **2** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenicated XSS (Cross-Site Scripting) 
  - [X] Summary: 
    - Vulnerability types: XSS (Cross-Site Scripting)
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.13
  - [X] GIF Walkthrough: 
    ![Alt Text](https://i.imgur.com/s5Zulon.gif)
  - [X] Steps to recreate: 
       * Create a new post while logged into a user acount
       * Insert the link into the text a youtube URL like https://youtube[.]com/watch?v=abc and then add to the end "< s v g on load=alert(1)>" 
       * When the post is viewed, the error should show
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

1. (Required) XSS(Cross-Site Scripting) Authenticated ShortCode Tags
  - [X] Summary: 
    - Vulnerability types: XSS (Cross-Site Scripting)
    - Tested in version: 4.0
    - Fixed in version: 4.3.1
  - [X] GIF Walkthrough: 
  ![Alt Text](https://i.imgur.com/PCJKfeR.gif)
  - [X] Steps to recreate: 
        * Switch to user with contributor permissions
        * Create a new post
        * Insert the following code into the HTML editor: [caption width="1" caption='<a href="' ">]</a><a href=" <Event-attribute-with-JS-code-here> ">Click me!</a>
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
    
    1. (Required) Authenticated XSS (Cross Site Scripting)
  - [X] Summary: 
    - Vulnerability types: XSS (Cross-Site Scripting)
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.3
  - [X] GIF Walkthrough: 
  ![Alt Text](https://i.imgur.com/Siuq2St.gif)
  - [X] Steps to recreate: 
        * Log into a user account
        * Create a new post
        * In the body of the post insert: <a href="[caption code=">]</a><a title=" onmouseover=alert('test') ">link</a>
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
   
