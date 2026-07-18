---
layout: default
title: "The app I never expected to build"
description: "I always wanted to build an app. For years I assumed it would be a tool, or a game, or some clever little utility. I never expected my first one to be a cycle tracker. I am not"
date: 2026-07-18
permalink: /devlog/origin/
canonical_url: https://nlarionov.github.io/mela-privacy/devlog/origin/
---
# The app I never expected to build

I always wanted to build an app. For years I assumed it would be a tool, or a game, or some clever little utility. I never expected my first one to be a cycle tracker. I am not the user. I did not have the problem. The problem sat across from me on a Valentine's trip.

![Mela's home screen: a calm cycle overview with the current day, phase, and next predicted period, no ads and no feed]({{ site.baseurl }}/devlog/images/screenshots/home.png)

## The moment

This February, my girlfriend and I went away for a few days around Valentine's day. At some point she opened her period app to log one detail about her body, the kind of thing you tap in and forget. Before she could do it, a full-screen ad loaded, the kind where you wait thirty seconds for the close button to appear. She sat and waited for it. Then another interruption, then finally the log.

I asked her why she still used the thing. Her answer was worse than the ads. She could not easily leave: five years of history in that app, and no export, no import, no migration path to anywhere. The monetization model had recently changed, so the ads were getting worse, and paying her way out made no sense either, because everything she needed was the basic functionality she already had. The subscription offered nothing she wanted. She was locked in, and her attention was the rent.

I watched this and something turned over in me. Here was an app that held some of the most intimate data a person has, treating her attention like inventory to be sold and her history like a hostage. To write one number about her own body, she had to pay in ads. It felt wrong in a way I could not shrug off.

Somewhere on that trip the idea clicked: why not build this myself? The app in front of me did not look impossibly complex. I had some basic Xcode and SwiftUI knowledge, a long-running habit of hanging around design resources, and now a user one seat away. It looked like a mountain I could actually climb.

## The one decision everything hangs on

There was one more thing she told me: she worried about where all that logged data goes and who might use it. That surprised me at first, so I started reading about the category. What I found did not make me feel better. The most popular cycle app in the world settled with the US Federal Trade Commission in 2021 over allegations that it shared intimate health data with third parties after publicly promising it would not ([FTC press release, January 2021](https://www.ftc.gov/news-events/news/press-releases/2021/01/developer-popular-womens-fertility-tracking-app-settles-ftc-allegations-it-misled-consumers-about)). The company neither admitted nor denied the allegations, which is how these consent orders normally end. Popular and trustworthy, it turns out, are not the same word. People trust these apps with more than they trust most humans, and the trust is not always earned. She was right to worry.

So I made a single decision and let everything else follow from it: the data should live only on the phone. Not in my cloud, because I would not have a cloud. Not behind an account, because there would be no account. Not in a third-party analytics kit, because there would be none.

If there is no server, there is nothing to leak, nothing to subpoena, nothing to sell, and nothing for me to be tempted by later when someone offers money for a data set I promised I would never build. Privacy by policy is a promise you make. Privacy by architecture is a promise you make impossible to break. I wanted the second kind.

That one choice turned out to decide almost everything downstream, and it cost me real things I will write about honestly in later posts. No crash reports. No usage analytics. No easy sync between devices. Support where I cannot look at the user's data even when they want me to. I took those costs on purpose. In this category I think they are the right ones.

## Building by listening

Here is the honest awkwardness of it. I am a man building an app about women's health. I do not have the body it is for. The only way I know to do that responsibly is to stop assuming and start listening.

So the app was built by listening. First to my girlfriend, who is patient with my questions and blunt about what is wrong. Then, as it grew, to other women who track their cycles and were willing to tell me what actually matters to them and what is noise. A lot of what I first thought was important turned out not to be. A lot of what I would have skipped turned out to be the whole point, like proper statistics and infographics, being able to look back over a year and see your own patterns clearly, which most apps bury or gate. That one came straight from her.

That listening is not a marketing line. It is the development process. When I am unsure, the answer is never "what do I think," it is "go ask." I keep building it the same way.

## What "solo, first app" actually means

There is no company here. No co-founder, no designer down the hall, no growth team. It is one person who writes the code, draws the icon, argues with App Review, writes the App Store copy in two languages, and then writes this. Every hat, one head.

That is slower and it is lonelier than a team, and it also means nobody in a meeting can talk me into a dark pattern for a quarterly number. The values in the app are just my values, unfiltered, for better and worse. If Mela ever betrays its own premise, there is exactly one person to blame, and he is writing this sentence.

![Mela's onboarding introduction: a warm, plain welcome screen that states the app's purpose without hype or cartoon styling]({{ site.baseurl }}/devlog/images/screenshots/onboarding-brand.png)

Mela is live now. Late June 2026, a quiet release, no splash, with a second version in July. Downloads run to a handful a day, and on the last full day of data I have it was four. I am going to be honest about numbers like that all the way through, because an app built to refuse manipulation would be a strange place to start manipulating you. Small and honest beats big and hollow, at least for now.

## What this series is

This is a build-in-public devlog, from the first idea to the App Store and past it. I will write about the architecture and what it costs, a genuinely strange technical problem I had to solve to let people bring their history over, the App Store review gauntlet, how you charge for a privacy app without becoming the thing you built against, and the launch numbers as they actually are.

It is written for other developers, which is a funny thing to admit, because you are not who the app is for. The people Mela is for are not reading a devlog about content-stream interpreters. That is fine. This series is not how I find them. It is where I show my work.

If you build things, the interesting question here is not "how do I get users." It is "what are you willing to give up to keep a promise." I gave up a lot. Next post, the exact bill.

---

*Mela is a tracker and a memory tool. It is not a medical device, a diagnostic, or contraception.*
