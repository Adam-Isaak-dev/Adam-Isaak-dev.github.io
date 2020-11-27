---
layout: post
title:  "TLS & SSL"
date:   2020-11-24 16:38:00 -0600
categories: blog-post writing-task
---

If you're anything like me, tech inclined and curious, you’ve probably had a point where you have wondered how your information is secured while wandering the internet. Well let’s jump down a rabbit hole of internet security, encryption, and cryptography, and learn about Transport Layer Security (TLS).

## A brief history
First some background. Back when computer networks were developing, much of the information transmitted was in plaintext (unencrypted information). That was until people started hacking. Now people could gain access to the data being transmitted and use it for themselves. Eavesdropping and other security risks led to the practice of encrypting the information while it was sent.

In 1986 a joint initiative between many communication and computer companies and U.S. departments started a project known as Secure Data Network Systems (SDNS).  SDNS was a research program focused on developing the next generation of secure computer communication. 

The SDNS program in 1993 developed Secure Network Programming as a method of securing transport layer API. Secure Network programming was designed to be similar to Berkeley sockets, thus allowing the ability to secure current network applications. 

Secure Network Programming eventually developed into Secure Socket Layer (SSL). SSL  2.0, was first published in 1995 with 3.0 being launched the following year. TLS 1.0 was launched in 1999 as an improvement to SSL with new protective methods. TLS 1.1 was published in 2006, 1.2 in 2008 and 1.3 in 2018. SSL 2.0 was deprecated in 2011, 3.0 in 2015, and TLS 1.0 and 1.1 were deprecated in 2020.

## How they work
Now that we know the history behind TLS how do they actually work? Putting aside the complex encryption algorithms, TLS works through a system of linked key pairs known as certificates. The public key can encrypt information that can only be decrypted by the private key. An example use is a public key set-up on a website, so that when a user creates an account it encrypts that data and sends it to a server that has the private key to decrypt the information.

Certificates are distributed through certificate authorities. Publicly trusted certificate authorities are implicitly trusted by certain software like browsers and operating systems. 
Upon connecting to the server the TLS handshake is started, the server transmits the certificate the user or browser confirms the certificate selecting the encryption level.

An aspect of TLS is HTTPS (Hypertext Transfer Protocol Secure), which is the secured version of HTTP. HTTPS uses encryption authentication from TLS protocol to secure data.

![Top-left of search bar](/assets/20-11-24/TLS_HTTPS.png)

*Here you can see if a website is using HTTPS indicated by both the extension and the padlock in the upper left corner of your browser.*

Here you can see if a website is using HTTPS indicated by both the extension and the padlock in the upper left corner of your browser.

## Why you should care
TLS is one of the major ways your daily internet usage is kept safe from those with ill intent. It pays to be aware of the steps you can take to stay secure on the internet. So next time you're on a site that shows an unlocked padlock, think long and hard about sending any information.

## Citations
> SSL Support Team. (2019, October 02). What is SSL? Retrieved October 17, 2020, from https://www.ssl.com/faqs/faq-what-is-ssl/

> Transport Layer Security. (2020, October 17). Retrieved October 17, 2020, from https://en.wikipedia.org/wiki/Transport_Layer_Security

> What is SSL, TLS and HTTPS? (n.d.). Retrieved October 17, 2020, from https://www.websecurity.digicert.com/en/ca/security-topics/what-is-ssl-tls-https