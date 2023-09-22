---
comments: True
layout: post
title: Pair Showcase Project
description: Project to showcase in live review with partner.
type: hacks
courses: {'compsci': {'week': 4}}
---

# Introduction

This page is a converted jupyter notebook of my and my partner's pair showcase project, which while being the fruit of a collaborative effort, is differing in some ways for each of us.

### Rating the Books I've Read So Far in 2023

| Author | Book | Month Read | Stars |
|------|-------|------|-------|
|Hafsah Faizal|We Hunt the Stars|January|4.5/5|
|Stephen King|Fairytale|April|4/5|
|Alex Aster|Lightlark|April|3.5/5|
|Colleen Hoover|It Starts With Us|April|3.5/5|
|Jennifer Lynn Barnes|The Inheritance Games|April|3/5|
|Jennifer Lynn Barnes|The Hawthorne Legacy|April|3/5|
|Jennifer Lynn Barnes|The Final Gambit|May|2.5/5|
|Ana Huang|Twisted Games|June|4/5|
|Colleen Hoover|Ugly Love|June|5/5|
|Ali Hazelwood|Love, Theoretically|July|5/5|
|Tahereh Mafi|Shatter Me|July|3.5/5|
|Tahereh Mafi|Unravel Me|July|3.5/5|
|Tahereh Mafi|Ignite Me|July|4/5|
|Tahereh Mafi|Restore Me|August|3/5|
|Tahereh Mafi|Defy Me|September|3.5/5|

## Basic Web Scraping 


```python
import requests 
from lxml import html

r = requests.get ("https://en.wikipedia.org/wiki/Book")
#print (r.text)

p1_xpath = """//*[@id="mw-content-text"]/div[1]/p[3]"""

if r.status_code == 200:
    tree = html.fromstring(r.text)
    p1x = tree.xpath(p1_xpath)
    for p1 in p1x:
        print(p1.text_content())
else: 
    print("Error retrieving web page.")
    
    
    
    


```

    A book is a medium for recording information in the form of writing or images, typically composed of many pages (made of papyrus, parchment, vellum, or paper) bound together and protected by a cover.[1] It can also be a  handwritten or printed work of fiction or nonfiction, usually on sheets of paper fastened or bound together within covers. The technical term for this physical arrangement is codex (plural, codices). In the history of hand-held physical supports for extended written compositions or records, the codex replaces its predecessor, the scroll. A single sheet in a codex is a leaf and each side of a leaf is a page.
    


## Shell script that returns a random number


```python
#import os

#os.system("""
          
#!bin/bash
#od -An -td1 -N1 /dev/urandom
           
          #""")

```

               75                                                            
    





    0


