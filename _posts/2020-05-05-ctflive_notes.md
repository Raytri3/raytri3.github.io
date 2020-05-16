---
author: Raymond_Gabler
layout: post
title: "CTF.Live Notes"
excerpt: "Notes from the CTF.Live Challenges."
categories: [Hack the Box]
---

I been playing around a little w/ CTF live and wanted to track my notes for the challenges I completed. As not to give away any spoilers (or viloate any of their rules), I wont go into too many details until the challenges are retired. You have to register w/ your gmail acount to access the site. CTF.Live is hosted by the folks at Pentester Acadamy.
> 
> This is the link: ctf.live


&nbsp;
---

# Webapps
 As of 05/052020 there wer 5 webapps. The goal of each was to gain a shell from the access given (either unauthenticated user or from the given user).

## Ecommerce
> After launching the site determine the software and version. Using that information google possible exploits. Once found, you have to modify the exploit to meet the parameters of the challenge. I suggest modifying the payload to make getting the flag easier. 

## Solr
> In this challenge you are given a kali instance to attack the website from which makes it a bit easier to get the flag. Search for metasploit modules to help you on your endeavours.  

## NMS
> This was a fun one, a bit different than the others. You are given a username and password to login into the CuteNews application. Once logged on you can upload information, and if you do it right you can upload shell code directly. HTTPTamper, Burp, Zap or some other proxy capability  will help you modify the data/shell.

## Rails
> For this challenge, you aren't given access to Metasploit but it is very helpful in completing this challenge. But as with most MetaSploit challenges, to include all those under the Metasploit category, you have to make sure you understand the exploit, the options, and the payload you want to use. On this challenge pay special attention to the payload and how you can use that to read a file (flag file) on a system.

# Beginner JWT 
Various challenges covering the basics of JWT tokens, to include breaking the keys and generating/forging tokens. The frustrating part was getting the tokens right.

## Secret in claim
> Given the name and password given generate a command to interact with the API. I chose to use CURL as it is an easy CLI to interact with site/apis. When using CURL make sure to include headers and the right json payload.

## Bruteforcing Weak Signing Key
> This challenge included two flags: 1. the key used to sign the JWWT 2. the flag stored on the system which is only accessible to an admin. Just like in "Secret in claim (SiC)", the first part is to get the first JWt token. If you're luckly enough to do SiC first this first part will be easy. Note that in addition to the token, make sure you take note of the user information json that is returned, as it will be need fot the last step. 
>Once you have the JWT token, you need to determine the signing key. Having access to Kali makes the proces of cracking the key, that and they used a weak key :).  Now that we have the key we can create our own token. I used jwt.io to do this part. As a little hint make sure you change the key to the one you cracked.

## Leaked Signing Key
> This challenge simulates a user posting information to public repoistory, like GIT. You are given access to the code which contains the JWT signing key. With a few well crafted Find or Grep commands you should be able to find the key. Once you hace the key follow the steps you did in Bruteforcing to create an admin user.

## None can forge JWT tokens
> Like the name implies, JWT can have none as their algorithm which makes spoofing the JWT easier. I used Cyberchef for this one as jwt.io doesn't allow (or I don't know how to do it) for None as the alogrithm.

## JWT Signature Leaks
> This one simulates a developer deploying troubleshooting logic to production. In this challenge you will get an error message when submitting the JWT, use the information provided in the URL to make modifications to your JWT.


