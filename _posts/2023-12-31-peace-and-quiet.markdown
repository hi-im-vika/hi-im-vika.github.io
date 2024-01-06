---
layout: post
title:  "Peace and Quiet"
date:   2023-12-31 23:23:00 -0800
categories: steam-deck repair
---
<!--2023-12-31-peace-and-quiet.markdown-->

> Edited since initial posting. Check the [commit history](https://github.com/hi-im-vika/hi-im-vika.github.io/commits/main/_posts/2023-12-31-peace-and-quiet.markdown) for earlier revisions!
—vika

# The Year (in review?)

2023 went by quickly, so quickly that I've forgotten about most of the cool stuff that I've done. I don't like making New Years' resolutions because I associate them with goals that I've set in the past and quickly neglected to work towards.

Instead, I like to consider that I recently found motivation to work on myself, and it's by pure coincidence that New Years' Eve is tonight. One of my goals is to start documenting the things I've learned and worked on. Hopefully, this will give me better insight into what I've been up to and help out others that might be struggling with the same problems I've encountered.

My first entry will be about my Steam Deck.

# The Deck

![steam deck !!!](https://cdn.cloudflare.steamstatic.com/steamdeck/images/press/renderings/press_oled_front_cocoon_thumb.jpg)

I got an OLED Steam Deck for Christmas because I transit a lot, leaving spare time on commutes that I can use to relax. Having this means I can play (almost) all my games everywhere I go.

# The Problem

Everything was great until I plugged in my headphones and heard the noise coming from the headphone jack. It's a buzzing/crackling noise that can be heard in the background of audio coming out the jack. I assumed it would go away once the device fully booted up, so I tried to ignore it. However, I still heard it after some time and got annoyed, so I switched to my AirPods.

Using them had their own issues as well. For example, the AirPods would occasionally disconnect and reconnect. As with the earlier issue, I tried ignoring it at first, but slowly became more annoying (both visual propmpts in SteamOS and the connection sound), so I began investigating how I could fix the noise coming from the headphone jack.

I could look at why my AirPods were disconnecting, but that felt more like a software issue, and I'm more interested in working with hardware.

I found a [video](https://www.youtube.com/watch?v=XuCFw-gfhlA) from [Tony Cassara](https://www.youtube.com/@TonyCassara) that detailed the same issue and a possible fix. Tony said that the fix didn't completely work for him, but I decided to give it a shot anyway.

# The Attempt

I began by removing the eight screws on the back of my Deck. The board with the headphone jack was located above the battery.

![steam deck headphone jack area](https://safe.vika.ws/0tR6dGnf.jpeg)

After removing the daughterboard, I noticed that there was a metallic outline under it. This suggested that the area was possibly conductive, meaning that it could be a source of noise, so I kept that in mind.

![steam deck headphone jack area with daughterboard removed](https://safe.vika.ws/Amctb29I.jpeg)

Following the video, I applied kapton tape to insulate the electrical contacts by the screws. Notice how the tape on the top left is not aligned properly—I'll get to that later.

![headphone jack daughterboard front side](https://safe.vika.ws/wDDFg3V0.jpeg)

Considering what I noticed earlier about the area under the daughterboard, I built upon the steps in the video and also put tape on the back of the daughterboard. I wanted to cover up anything that could pick up noise as much as possible.

![headphone jack daughterboard back side](https://safe.vika.ws/X8WQJcvz.jpeg)

# The Mistake

After reassembling everything, I was pleasantly surprised to see (or hear) that the noise was gone! I wanted to write something about what I did, but realized that I forgot to take pictures of my work, so I disassembled the Deck again.

When I finished reassembling again, the noise returned, so I inspected the tape around the screws. Turns out that some of the tape warped while tightening the screws, so I reapplied it. This was the reason behind why the tape in one of the earlier photos wasn't aligned.

# The Result

After doing that and reassembling everything, there was no noise anymore, as expected from earlier. Satisfied with my accomplishment, I moved on to getting my Steam library and emulators onto my Deck. Little did I know, this would be the first of many small things I'd have to troubleshoot as I continued to use the Steam Deck...