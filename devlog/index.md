---
layout: default
title: "Mela devlog"
description: "Building Mela in public: a private, offline iPhone cycle tracker, from idea to the App Store."
date: 2026-07-18
permalink: /devlog/
canonical_url: https://nlarionov.github.io/mela-privacy/devlog/
---
# Mela devlog

A build-in-public journal about making **Mela**, a private, offline cycle tracker for iPhone, by one developer, as his first app.

## What Mela is

Mela is a cycle tracker built on a single idea: intimate health data should live only on your phone. There is no server, no account, and no third-party SDKs. Nothing to leak, nothing to subpoena, nothing to sell. The App Store privacy label reads Data Not Collected in every category, because that is what the architecture actually produces, not a slogan.

It does what daily tracking needs. Period and ovulation predictions, a calendar with phase markers, quick logging of symptoms, mood, and intimacy, reminders you set yourself, and monthly and yearly analytics that turn your own logs into clear patterns over time. Your history imports from another app and exports in full, any time, and it can read from Apple Health if you turn that on. And it stays calm on purpose: no content feed, no streak mechanics, no nudges, no notifications beyond the ones you choose.

Mela is a tracker and a memory tool. It is not a medical device, a diagnostic, or contraception, and it does not pretend to be.

- **Built with:** 100 percent SwiftUI, zero external dependencies, iOS 17 and up, iPhone.
- **Data:** local JSON, file-protected and encrypted at rest, on your device only.
- **Apple Health:** read-only and opt-in, off until you turn it on. Nothing is written back, nothing leaves the phone.
- **Not included, on purpose:** no cloud, no login, no analytics, no ad SDK, no crash reporter.
- **On the App Store:** Mela: Private Cycle Tracker. [App Store link](https://apps.apple.com/app/mela-private-cycle-tracker/id6777094477)

## Why this devlog exists

This is where I show my work: the decisions, the trade-offs, the engineering, and the honest numbers, from the first idea through the App Store and beyond. It is written for other developers. If you build things, especially privacy-minded things, this is the part of the story most launches leave out.

A note on honesty: the app was built to refuse manipulation, so the writing refuses it too. Numbers are stated plainly, including the small ones. Nothing here is dressed up.

## The series

Written to be read in order, but each post stands alone.

1. **[The app I never expected to build]({{ site.baseurl }}/devlog/origin/)** - the origin story. Why a solo developer with no stake in the category built a cycle tracker, and the one decision everything else follows from.
2. **Privacy by architecture, and what it costs you** (coming soon) - the difference between private by policy and private by architecture, and the real engineering bill for having no server, no analytics, and no crash logs.
3. **Importing a competitor's PDF by reading its vectors, on device** (coming soon) - the standout technical story. An on-device PDF content-stream interpreter that recovers years of history from a competitor's visual export, offline, and a test that proves it matches its Python reference on 536 of 536 events.
4. **100 percent SwiftUI, zero dependencies** (coming soon) - the architecture that made a no-package build practical, and where that choice actually costs you.
5. **The App Store review gauntlet** (coming soon) - the rejections, by guideline number, and the specific fixes. The part that is harder than the code.
6. **Charging for a privacy app without betraying the premise** (coming soon) - a pricing model with no dark patterns, and how you validate purchases with no server.
7. **Launch, and the honest numbers** (coming soon) - what shipping actually looked like, and the real, small figures, without the growth-curve theater.
8. **Calm by default: building against engagement dark patterns** (coming soon) - restraint as a design discipline, and what it costs in the metrics most apps live on.

New posts land every few days. Start with post 1. Post 3 is the technical one, and it is the one to watch for.

## About

Mela is made by Nikita, a solo developer. It is built by listening to the women who use it. If you want to reach me, email [dace_phoenix_2p@icloud.com](mailto:dace_phoenix_2p@icloud.com).

- App Store: [Mela: Private Cycle Tracker](https://apps.apple.com/app/mela-private-cycle-tracker/id6777094477)
- Privacy policy: [Mela privacy policy]({{ site.baseurl }}/)
- Source-code structure is auditable on request by independent researchers.
