---
layout: post
title: Git - find unmerged commits
date: 2016-03-22 12:57:35.000000000 -05:00
type: post
published: true
status: publish
comments: true
category: programming
tags: 
  - git
  - ruby
author:
  login: miroadamy
  email: miro.adamy+blog@gmail.com
  display_name: miroadamy
  first_name: ''
  last_name: ''
---

# Git - find unmerged commits

This is Ruby script I found way back and was using it since. 

The credits for creation goes to Zach Dennis. The script is decribed in his 
[blog post](https://www.mutuallyhuman.com/blog/2009/07/02/finding-unmerged-commits-with-git-unmerged/)

The source [is here](https://github.com/mhs/tidbits/blob/master/lib/git-unmerged.rb)


### Example

This is beginning of very long output from Groovy source

<img src="{{ site.baseurl }}/images/2016-03-26_20-45-36.png" alt="" width="700"  />

### The code 

{% gist f5c81819219f6f9e2fdf %}