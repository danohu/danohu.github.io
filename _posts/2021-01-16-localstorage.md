---
layout: post
title: Firefox bug workaround -  NS_ERROR_FILE_NO_DEVICE_SPACE
date: 2021-01-16
---

You probably don't want to read this, unless you got here by googling the error message. Just a bug workaround, which I've backdated into the archives so it gets to exist somewhere online.



**The problem**: Most websites which use localstorage stop working. You look in the console, and find many errors NS_ERROR_FILE_NO_DEVICE_SPACE. But there is plenty of space on your hard drive



**The solution**: delete storage.sqlite in the firefox profile directory



**What's going on**: the sqlite database that manages localstorage got corrupted (perhaps because the disk _was_ full at some point). Delete the  database and firefox will happily recreate it.



...At least, that's what worked for me. No guarantees!