---
layout: default
title: "The app I never expected to build"
description: "I always wanted to build an app. For years I assumed it would be a tool, or a game, or some clever little utility. I never expected my first one to be a cycle tracker. I am not"
date: 2026-07-18
permalink: /devlog/origin/
canonical_url: https://nlarionov.github.io/mela-privacy/devlog/origin/
---
# The app I never expected to build

I always wanted to build an app. For years I assumed it would be a tool, or a game, or some clever little utility. I never expected my first one to be a cycle tracker. I am not the user. I did not have the problem. The problem sat across from me on a Valentine's trip. Honestly, I still do not fully believe I pulled it off. Here is how the idea found me and what the road actually looked like.

![Mela's home screen: a calm cycle overview with the current day, phase, and next predicted period, no ads and no feed]({{ site.baseurl }}/devlog/images/screenshots/home.png)

## How it started

This February my girlfriend and I went away for a few days around Valentine's day. At some point I watched her open her period tracker, and once again the app hit her with ads first. The kind where you wait 30 seconds for the X to appear, close the ad, and only then get to log your period.

I asked her: why do you still use this thing? I personally hate ads in apps. If an app is valuable to me, I try to pay for it, or I look for an open source alternative.

Her answer stuck with me. She could not easily leave. Five years of history in that app, and no export, no import, no migration path to anywhere. Meanwhile the app had recently changed its monetization model and the ads got completely out of hand. Paying did not make sense to her either: everything she needed was the basic functionality she already had, and the Pro subscription added nothing she actually wanted. Why should she suddenly pay just to keep logging the same things she had been logging for five years?

## The idea

That is when it clicked: why not try to build this myself? I looked at the app and it did not seem impossibly complex. I had some basic Xcode and SwiftUI knowledge, and in my free time I had always enjoyed hanging around design resources. So I figured: why not.

I started digging into the category and looking at the current players. And I kept interrogating my girlfriend, probably driving her a little crazy with my silly questions. What is missing? What is critical? What would actually make you switch?

Two things came up over and over. She badly missed proper infographics and statistics, some way to actually see her own patterns instead of just a calendar. And she worried about where all that logged data goes and who might use it.

## The privacy rabbit hole

That worry surprised me at first, so I started reading. What I found did not make me feel better. The most popular cycle app in the world settled with the US Federal Trade Commission in 2021 over allegations that it shared intimate health data with third parties after publicly promising it would not ([FTC press release, January 2021](https://www.ftc.gov/news-events/news/press-releases/2021/01/developer-popular-womens-fertility-tracking-app-settles-ftc-allegations-it-misled-consumers-about)). The company neither admitted nor denied the allegations, which is how these consent orders normally end. Popular and trustworthy, it turns out, are not the same word. People trust these apps with more than they trust most humans, and the trust is not always earned. She was right to worry.

So privacy became the core of the whole project. I made a single decision and let everything else follow from it: her data should live only on the phone. No server, no account, no analytics, no ads. If there is no server, there is nothing to leak and nothing to sell.

And that five-years-of-history lock-in? It turned into the first genuinely hard technical problem of the project: I built an importer that recovers her entire history from the old app's PDF export, fully on device.

## Building by listening

Here is the honest awkwardness of it: I am a man building an app about women's health. I do not have the body it is for. The only way I know to do that responsibly is to stop assuming and start asking. So the app was built by listening. First to my girlfriend, who is patient with my questions and blunt about what is wrong. Then to other women who track their cycles. A lot of what I thought was important turned out to be noise, and a lot of what I would have skipped turned out to be the whole point.

## The road there

From that February idea to a live app took me about four months of evenings. There is no company behind it: one person writes the code, draws the icon, argues with App Review, and writes the App Store copy in two languages. Several TestFlight cycles with my girlfriend as the first and harshest tester. A lot of talking, a fair amount of misunderstanding, endless questions from my side, pointed questions from hers, and criticism that sometimes stung and always made the app better.

And then App Review. I went through several rounds of rejections, fixed what was fair, pushed back where I disagreed, and eventually got through. Per aspera ad astra. The rejection-by-rejection story is a saga of its own.

![Mela's onboarding introduction: a warm, plain welcome screen that states the app's purpose without hype or cartoon styling]({{ site.baseurl }}/devlog/images/screenshots/onboarding-brand.png)

## It is live

The app quietly went live in late June 2026, with a second version in July. It is small, downloads are a handful a day, and I am strangely fine with that. Seeing real people use something you made is a feeling I can not quite describe. An app built to refuse manipulation would be a strange place to start manipulating people with a fake growth story, so the numbers I share will always be the real ones.

## Why I am telling you this

If you have ever dreamed of building your own app: do not wait. If you have an idea, you can absolutely pull it off. From the first spark to a live App Store page can take way less time than you think, and the tools and knowledge available today are more than enough.

I write the whole journey up in detail on my devlog: the architecture and what it costs, the PDF importer story, the App Store review gauntlet, and the real numbers as they come: https://nlarionov.github.io/mela-privacy/devlog/

The app itself, if you are curious: https://apps.apple.com/app/mela-private-cycle-tracker/id6777094477

Good luck out there, I hope you get to ship the app of your dreams. Have a great day, and wishing you all fewer bugs and zero memory leaks :)

---

*Mela is a tracker and a memory tool. It is not a medical device, a diagnostic, or contraception.*
