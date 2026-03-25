---
layout: post
title: "Challenge: Build an Insurance Policy Admin System in 2 Days Using AI"
date: 2026-03-25
categories: [AI, Insurance, React]
---

Could one person build a full insurance policy admin system in 2 days? I decided to find out.

In previous posts I have documented how Claude AI can build beautiful user interfaces for small use-cases, and even recreate a UI from just a screenshot. But what about something far more ambitious like, say, an entire frontend for a Policy Administration System?

Spoiler: it can be done. In this article I will walk through how I did it, what went well, what didn't, and I'll share a working link so you can try the result yourself.

---

## The Problem To Solve

A few years ago a friend worked for one of the largest social media companies in the world. That company had embraced a radical idea: one single web-based system for every job role. No Excel, no off-the-shelf tools, no fragmented software sprawl. Licence costs were minimised, processes were enforced, and everything lived in one place.

I thought the idea was genius. So I set out to apply it to the insurance world, One Insurance System: a single platform that handles policies, claims and quotes under one roof.

---

## My Approach

Rather than writing code by hand, I used a method that has become known as vibe coding, describing what you want to AI in plain language and letting it produce the code for you. You then paste the output into the right places in your project and iterate from there.

---

## The Result

Here is the live application that Claude and I built together:

**[kind-dune-017ce2910.6.azurestaticapps.net](https://kind-dune-017ce2910.6.azurestaticapps.net/policies)**

Desktop Version

![Desktop Version]({{ site.baseurl }}/assets/images/ClaudeVibeCoding/desktop-version.png)

Mobile Version

![Mobile Version]({{ site.baseurl }}/assets/images/ClaudeVibeCoding/mobile-version.png)

---

## What Went Well

The aesthetics were excellent out of the box. Claude produced a clean, professional interface with a consistent purple accent colour, readable typography, and a layout that feels like a real enterprise product. I didn't spend any time manually tweaking CSS.

The mock data was remarkably realistic. All the people, policy numbers and claim references in the application are entirely fictitious, and I never once asked Claude to generate them. It produced plausible insurance data entirely on its own initiative, which made the product feel more realistic.

Insurance domain knowledge was largely handled well. I didn't feed Claude my LM1 and LM2 exam knowledge. It correctly used terms like Gross Written Premium, No Claims Discount, Mid-Term Adjustment, and named relevant insurers. There are a few minor terminology nuances such as how an insurance professional might prefer "endorsement" in certain contexts over "mid-term adjustment", but nothing that a quick edit wouldn't fix.

The entire project cost nothing. The free tier of Claude built the app. Azure Static Web Apps hosts it for free. GitHub stores the code for free. The deployment pipeline from GitHub to Azure is free. **Total spend: £0.**

---

## What Didn't Go Well

Mobile support was an afterthought. Claude didn't build for mobile initially, I had to ask. When I did, some elements scaled off-screen. It took a few back-and-forth exchanges to get there. Starting with a mobile-first mindset from the beginning would have saved time.

A Tailwind CSS configuration issue caused a crash. Midway through the project the application crashed and I had to prompt Claude to investigate. We eventually traced it to missing content path references in the Tailwind config. It's a reminder that vibe coding still requires an understanding of software engineering to know when something looks wrong.

The favicon took two attempts. I asked Claude to crop just the shield from my logo to use as a favicon. The first attempt included a sliver of the text beside the shield. A second pass fixed it cleanly, but it's an example of where a quick visual check before committing would have saved a round trip.

The initial scaffold needed a lot of iterations. The first version was a basic shell. The search bar, user profile dropdown, AI assistant sidebar, sub-menu navigation, mobile drawer, and all the individual page content had to be requested separately. Over two fairly intense days (and I mean full days, not business days) we got to something genuinely impressive, but it required sustained focus and direction throughout.

This is a frontend, not a finished product. The application has no backend. There is no authentication, no real data, no API, no database, and no security hardening. Making it production-ready with user roles, data persistence, scalability and compliance, would realistically require another four to eight weeks of solid work, even with Claude's assistance.

---

## Final Thoughts

Yes, you can build a credible insurance policy admin system frontend in two days using AI. Yes, you will hit problems along the way. And yes, a significant amount of work remains before something like this is ready for real users.

But the key takeaway is this: Claude doesn't replace software engineers, it assists them. An engineer working with Claude can move at a pace that simply wasn't possible before.

I hope you enjoyed reading this post. In my next post I will be taking on an even bigger challenge: designing the full system architecture needed to take One Insurance System from prototype to production.

---

**If you have a legacy system that needs rebuilding, or a product idea that needs a frontend, I would love to discuss it with you. I am currently available for new engagements.** 
