---
title:  "Tools for a more mindful Internet and Social Media experience"
linktitle:  "Tools for a more mindful Internet and Social Media experience"
date:   2024-06-10
categories:  ["Computer Science", "Misc"]
tags: [ "programming"]
---



{{< table_of_contents >}}



## Intro
This quick blogpost wil be mostly a categorization for myself about some general tools I use to make social media and internet browsing more useful and a generally better experience (for me at least). I've been programming for more than 12 years (at the time of this blogpost), and working within the technology industry for more than 5 years. I've seen a lot of tools and I've tried a lot of them, but these are the ones that I've been using for a while and that I think are worth mentioning.

Just a caveat: I'm not affiliated with any of these tools, I'm just a user that found them useful. I'm also not a "productivity coach" or anything like that, so I don't go on a constant search for new tools. I just use what I find useful and that's it.

> **Important**: The most important thing is not actually the tools, but how you actually browse the internet and use social media. I won't explain this here, but you can find useful resources about how I generally approach it based on the books [Digital Minimalism](https://www.amazon.com/Digital-Minimalism-Choosing-Focused-Noisy/dp/0525536515) by Cal Newport and [Stolen Focus](https://www.amazon.com/Stolen-Focus/dp/1526620227) by Johann Hari. I mostly shaped my approach based on these books and my experience over the years. 

## What are the core values of how you use the internet?

Before I start, I think it's important to understand what are the core values you want to have when using the internet - these will vary from person to person, it doesn't matter the specifics, but the most important thing is actually thinking about it. Most people will just use the internet without thinking about it, or just start using something new without actually giving a thought about how it serves them.


### Minimizing enshittification

A general phenomenon within internet usage, [enshittification](https://en.wikipedia.org/wiki/Enshittification) is the process of a product becoming worse over time. This is being constantly applied to social media platforms, but it's not exclusive to them. In the age of LLMs, where automatically generated content is becoming more and more common, I feel I have to constantly be "fighting back" against this process.

I'm not naive enough to believe that using a certain toolbox will make us immune to this process - falling into the trap of delegating a societal problem to personal, individual solutions is a common practice of neoliberalism. However, I think that by being mindful about the tools we use, we can at least minimize the impact of enshittification on our lives.


### Minimizing signal-to-noise ratio

In the beginning of my student years I tried to maximize the content I consumed - I followed a considerable number of newsletters, podcasts, followed a lot of people (from my area but also a lot of other stuff) on social media, engaged in a lot of forums, etc. For a time this can be useful, especially to getting to know core concepts, understanding different ideas, i.e. it's very good for exploring the whole "knowledge space" of a certain area/interest.

However, as I got into more specific areas of interest, I felt the need to really trim down the content I was consuming. I started to unfollow people, unsubscribe from newsletters, etc. I started to think about the signal-to-noise ratio of the content I was consuming. I want to maximize the signal (the useful content) and minimize the noise (the content that doesn't add value to me).

From time to time I do a "content curation session" - I go through my social media, newsletters, etc, and see if the content is still useful to me. If it's not, I unsubscribe, unfollow, etc. This generally works by:

- Unfollowing/muting content that doesn't add value to me
- Specifically trimming down the content I consume to the most useful/trusted sources
- Algorithmic curation: For certain social media, try to "train" the algorithm by giving explicit feedback on the content you want to see
- Use tools to minimize the noise (I'll talk about them below)

> Time is a (very) limited resource, so one of my core values **now** is to minimize the noise and maximize the signal of the content I consume. This drives how I mostly approach the tools I use, if I actually use them or not, and most importantly, **how** I use them.

## Vivaldi Browser

My main browser, now for several years. I've used Chrome, Firefox, Opera, Safari, etc, but Vivaldi is the one that I've been using for a while now. It's a Chromium-based browser, so it's very fast, but it has a lot of features that I find useful:

- Tab Stacks: I can group tabs together, which is very useful for when I'm working on a project and I need to have a lot of tabs open
- Tab Tiling: I can tile tabs, which is useful for when I'm working on a project and I need to see two tabs at the same time
- Chromium-based browser enables me to use Chrome extensions, which is very useful
- Customizable: I can change the theme, the layout, etc. I especially use this to minimize the noise of the browser itself - I use a dark theme, I hide the bookmarks bar, etc.
- Workspace: I can create different workspaces, which can be used to separate different scopes of work.
- Command Palette: I can search for tabs, settings, etc, using a command palette. Once you get used to it and its shortcuts it makes the browsing experience much faster.

A lot of stuff you see on newer and trendy browsers (e.g. Arc) are actually built-in features that always were present on Vivaldi. Here's an example of my current interface (here on Windows 10):


{{< image
    src="/img/vivaldi.png"
    alt="Good" >}}

The interface is very clean - I use a simple dark theme, I don't have a bookmarks bar, I use the tab stacks feature to stack related tabs together. I specifically removed some features that I don't use, like the status bar, icons for features I rarely use (or when used is through the command palette, not clicking in it), and I specifically removed most extensions and only keep on the interface the ones that actually I constantly will have to interact with.

## Extensions

To really take advantage of the browser, I use some extensions that I find really useful. I try to keep them in a small number to not slow down the browser. Here's the current list of extensions I use:

### General

- **uBlock Origin**: The best adblocker out there. A must-have extension in today's internet, without it the browsing experience is just unbearable.

- **Vimium**: Navigate the browser using Vim-like shortcuts. It's very useful to navigate the browser without using the mouse. (No, I don't use Vim, but I like the shortcuts).

- **Dark Reader**: Dark mode for every website... I can't live without it anymore.

- **Momentum**: A new tab page that shows a beautiful picture, a quote, and a to-do list. I mainly use this because I'm not a fan of speed dials...

- **AutoplayStopper**: Stops autoplay on websites. There's few things more annoying than autoplay videos, this extension stops them.

- **I still don't care about cookies**: Removes cookie warnings from (most) websites

### Productivity related

- **Strict Workflow**: A Pomodoro timer that blocks websites that you define as distracting.

- **TimeYourWeb Time Tracker**: I use this extension to track the time I spend on websites. Mostly for personal analytics.

- **RescueTime**: Also used for time tracking, but this one is more general


### Social Media related

- **Video Speed Controller**: Control video speed on any website. I use this a lot on Youtube, but also on other websites that have video content.

- **SponsorBlock**: Skip sponsored segments in Youtube videos.

- **Hide youtube shorts**: Hides Youtube shorts from the homepage. I don't like them, so I just hide them.


- **Reddit Enhancement Suite**: Enhances the Reddit experience. I use it to filter out subreddits, users, etc.

- **Fluff Busting Purity**: Removes a lot of the noise from Facebook. Allows to remove a lot of stuff from the feed, like sponsored content, meaningless posts/updates, useless sections, etc.

- **Control Panel for Twitter**: Similar to Fluft Busting Purity, but for Twitter. Allows to remove a lot of useless stuff from the feed, keeping the experience focused on the content I want to see.


## (extra) Mobile tools

On my phone I barely use social media - however, I do use some tools to make the experience better. Here's a quick rundown of the tools I use:


- **Firefox Browser**: I use Firefox on the phone as it has ad blocking built-in, and I can easily add extensions. I know there's some better and more configurable browsers out there, but I'm used to Firefox and it works well for me.

- **Aeroinsta**: An Instagram client that doesn't show ads, doesn't track you, etc. It's a very simple client, but it works well for me. There's some advanced features that I use like removing specific sections of the app, such as suggested posts and removing reels.

- **Youtube revanced**: Must-have Youtube client. It has a lot of features that the official app doesn't have, like background playback, ad blocking, etc.
