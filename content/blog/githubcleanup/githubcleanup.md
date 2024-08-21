---
title: Cleaning Up My GitHub for a New Project
description: Writing about cleaning up my GitHub repos in anticipation of a fun new project.
date: 2024-08-20
tags:
  - github
  - cleanup
draft: false
---
I want to work on a new, exciting software project. But, whenever I try to get started I feel guilty about all the PRs, dependabot alerts, and old code I haven't addressed in my GitHub account. Seeing all of that pile up saps my motivation, but I'm sure I can take a week to get everything in order. My upcoming project is a clone of [The Kingdom of Loathing](https://www.kingdomofloathing.com/) using [SpringBoot](https://spring.io/projects/spring-boot) and [htmx](https://htmx.org/). Stay tuned for Game Design, Architectural Design, and more from my upcoming project!

With that introduction out of the way, let's go though my existing non-archived projects and see what I'm going to have to do to get this all cleaned up.

## [backlog_puller](https://github.com/GTmmiller/backlog_puller)

This is a simple command-line utility for pulling game data from [The Backloggery](https://www.backloggery.com/). I originally created it to retrieve data for spreadsheets and amateur data science stuff and thought other people might find it useful too.

I recently got an email from the German research institute [fortiss](https://www.fortiss.org/en/) asking me about this package and I remembered that I left a few PRs hanging. The Backloggery recently had a [total redesign](https://www.patreon.com/posts/remake-launch-104736678), so I suspect I may have to retire this project entirely, which would really be the end of an era for me. This has been my most successful personal software project in terms of overall engagement and usage.

### Action Items
- Check if the redesign is compatible with the PR changes to update to Python 3
- Potentially EoL the project if it no longer works
    - Remove or mark as archived in PyPi
    - find my pyPi credential

## [Saga Frontier Combo Simulator](https://github.com/GTmmiller/saga-frontier-combo-simulator)

I don't like the original Saga Frontier, but the 2021 remaster was my game of the year when it came out. I enjoyed it so much that I created a simulator for the game's combo system. It even did some small numbers [in the SaGa subreddit](https://www.reddit.com/r/SaGa/comments/xmx7dj/saga_frontier_combo_tool/).

I used full-strength Vue for this project. It was a good decision at the time, but looking at it now it feels like it was a little overkill. It doesn't call any apis and it's pretty much a simple one page tool. For now, I'll just update dependencies and make sure all the tests pass, but a rewrite using a lighter framework like [alpine.js](https://alpinejs.dev/) would be a fun project.

### Action Items
- Update out of date dependencies
- Update node version to latest lts (v20)
- Ensure all tests pass and it works as expected
- Cut and deploy a new web release

## [Plump](https://github.com/GTmmiller/plump)

This distributed lock service was originally going to be part of a series of projects I did as a supplement to my grad school coursework. Turns out, map reduce is much easier to model than distributed locking! I wanted this to take 1 month, but three years, and two language changes later it was finally done. I want to keep this around as long as I can since I use it as a reference project for a lot of setup I do in Java projects like setting up Unit Testing, Checkstyle, and multiple modules.

### Action Items
- Turn on Dependabot warning
- Update any out of date dependencies
- Cut a new updated release if needed

## [brainf-inter](https://github.com/GTmmiller/brainf_inter)
An interpreter of the [Brainfuck langauge](https://en.wikipedia.org/wiki/Brainfuck). Though the name is a little crude, it's basically a simple language for representing a Turing machine.

I've kept this project around because it's a fun blueprint for a javascript library that works on the browser and on Node at the same time. It's not very useful, but it's pretty lightweight and fun to keep around.

### Action Items
- Update dependencies
- make sure the latest lts verison of Node is called for
- check if this is still best practice for a package for the browser and nodejs
- Redeploy to npm

## Archiving

I have a bunch of old projects that I don't want to maintain anymore, but I like to keep around for sentimental or other reasons.

**hex-game** - An incomplete implementation of the game [Hex](https://en.wikipedia.org/wiki/Hex_(board_game)). I might revisit this in Godot as a simple game exercise.

**hde-twitter-like** - A twitter clone I made for an internship that I quite enjoyed. Not going to update this one any time soon, but I have some great memories from that internship. Checkout the [Hennge global internship program](https://hennge.com/global/gip.html) if you're interested in working and living in Tokyo for a bit.

**pokego-evol-maximizer** - This was supposed to calculate the amount of pokemon you can transfer to maximize the number of pokemon you could evolve from the candy resulting from the transfer. This never quite worked correctly, but it gave me lot of valuable experience with numpy.

**bankinator** - I made this application to sign into my bank account and pull information. The bank I wrote this for is now defunct and this was before the days of open banking apis. It doesn't work and I don't want to update it.

## Moving Forward

I'm excited to get cleaning and to move on to my next project! Next post should be next week detailing how the clean up went and I should get some time to start writing up the intro to the new project.

See you in the next post!

