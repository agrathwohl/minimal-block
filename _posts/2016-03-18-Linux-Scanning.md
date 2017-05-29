---
layout: post
title:  "Smart Document Scanning in Linux"
date:   2016-03-18 00:00:00
categories: computing
tags: brother, scanner, documents, paperwork
---

I recently purchased a [Brother ADS-1000W](http://www.amazon.com/Brother-ADS1000W-Compact-Wireless-Networking/dp/B00EKW6JGI/ref=sr_1_1/189-6315539-7444747?ie=UTF8&qid=1458354800&sr=8-1&keywords=brother+ads+1000w), a nifty and tiny document scanner that has rather good support in Linux.

After obtaining some necessary software and doing a bit of troubleshooting, I got my Arch Linux system scanning documents and parsing the resulting images for searchable strings. This means - yes - you can scan all of your loose documents and thus maintain a dated and tagged repository of all your shit!

First things first, you'll need to obtain the [Brother drivers from the AUR](https://aur.archlinux.org/packages/brscan4).

Once you've installed brscan4, go ahead and run `pacman -S simple-scan` to get a good lightweight scanning app. That should be all you need to do to start scanning documents!

If you find that simple-scan doesn't recognize your Brother scanner, you may need to engage in some trickery which is well-documented over on the [Ubuntu user forums](http://askubuntu.com/a/447283).

Supposing you're one of those *super hardcore* types, you could always look into obtaining the fantastic [Paperwork](https://github.com/jflesch/paperwork), a Linux-only app developed to scan and parse documents via a 1000W-esque device.