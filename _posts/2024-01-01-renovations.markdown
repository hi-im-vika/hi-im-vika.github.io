---
layout: post
title:  "Deck Renovations"
date:   2024-01-01 13:21:08 -0800
categories: steam-deck
---

SteamOS is already nice, but I want to customize the desktop interface exactly the way I want it. I like that SteamOS is based on Arch Linux because I've used it before and I liked how I could customize almost anything on my installation. Understandably, the Arch install for SteamOS isn't a regular installation, so there were some things I needed to troubleshoot.

This is a compilation of a couple tweaks I've applied to my Steam Deck, with instructions found from various places on the web with sources listed.

# Getting `pacman` to Work

I wanted to install some custom fonts on my Deck, so I needed to use `pacman` and also install `yay`. However, SteamOS protects its system files with read-only permissions to avoid accidentally them up. I need to be able to modify those files to update the keyring and install packages, so I disabled the read-only protection. I found a reddit post (linked below) that explained how to do this.

Originally, I thought that I could get away with only disabling the read-only protection to get `pacman` working, but it turns out that the `pacman` keyring is empty. This means that SteamOS has no way to verify the authenticity of its downloaded packages, so I fixed that first. [This reddit post](https://www.reddit.com/r/SteamDeck/comments/t8al0i/install_arch_packages_on_your_steam_deck/) by [u/awkisopen](https://www.reddit.com/user/awkisopen/) provided a clear explanation for what to do.

Here's what I did:
1. Set a password:
```
passwd
```
2. Disable SteamOS read-only protection:
```
sudo steamos-readonly disable
```
3. Init pacman keyring:
```
sudo pacman-key --init
```
4. Populate the keyring with archlinux keys:
```
sudo pacman-key --populate archlinux
```
5. Do the same with the SteamOS holo keys[^1]:
```
sudo pacman-key --populate holo
```
If this step doesn't work, try replacing `holo` with whatever the codename is for your current SteamOS version.

After I completed the last step, I did `pacman -Syu` to make sure that everything worked and apply any available updates.

# Applying the Font

Coming soon...

# Applying Dark Mode

Coming soon...

# References
[^1]:https://www.reddit.com/r/SteamDeck/comments/t8al0i/comment/kaf7d91/