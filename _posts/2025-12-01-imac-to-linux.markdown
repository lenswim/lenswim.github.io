---
layout: post
title:  "IMac To Linux"
date:   2025-12-01 15:25:31 +0100
categories: imac linux
---

## Why?

* super slow after 14 years
* not upgradeable because of limit specs
* chrome browser not upgradeable because OS was too old
* I wanted a personal machine to do some programming stuff
    * I was too lazy to set up multiple SSH keys on my work laptop to support 2 github accounts

## Bootable USB
1. Download .iso file for Linux Mint
2. > Probably not the "easy" way, because it's not graphical. But it is kinda pretty easy.

Open terminal (press cmd+space and type "terminal")

First type "diskutil list" and press enter

then insert your usb stick and run "diskutil list" again to see the disk node (e.g. /dev/disk2)

Now run "diskutil unmountDisk /dev/diskN" (where N is the number of the usb stick)

and then run "sudo dd if=/path-to.iso of=/dev/rdiskN bs=1m"

(after typing "sudo dd if=" you simply copy paste the path that's to be found when you right click on the file, then click "get info" and copy the path under "Where")

When finished "diskutil eject /dev/diskN" \\> — <cite>[dude op reddit](https://www.reddit.com/r/mac/comments/6tltiw/how_do_i_easily_burn_a_bootable_iso_to_a_usb/)</cite>

## Installing Linux
1. insert USB
2. hold alt-button on keyboard
3. turn on IMac
4. select USB device
5. follow installation guide

## More RAM
My 2011 IMac had 4GB RAM out of the box, but apparently it supports up to 32GB.

On the bottom of the screen frame there are 3 screws that you can unscrew to open to RAM slots.

There are some black plastic flappy things that you can pull to eject/insert the RAM sticks

## Installing Node (to build a react app)
sudo apt-get install -y nodejs -> v18.19.1

Apparently nodesource has it's own repository for node packages:

`curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -`

This basically says "yo, if someone asks for node stuff, go to nodesource".

## Installing Docker Engine
Same as node, custom repo via https://docs.docker.com/engine/install/ubuntu/

## Installing Docker Desktop
[Docker documentation](https://docs.docker.com/desktop/setup/install/linux/ubuntu/)