---
layout: post
title: "Claude Code - The good and the bad"
date: 2026-06-01
categories: [AI]
---
I have recently been giving Claude Code a thorough road-test. I've been very demanding in my requests; I asked for Stripe credit card payments, Azure Storage to save files, an Azure Cosmos Database for high availability and scalability, QR code generation, Microsoft, Google and local account registration and login, and very specific processes for how to structure outputs.

In this blog post, I will outline the good and the bad and give my honest opinion on Claude Code as it stands today.

---

## What is Claude Code and How Does it Work?

Put simply, Claude Code is an extension that you can install into a code IDE (Integrated Development Environment) such as Visual Studio Code. As long as you pay for Claude Professional or above, you tell Claude Code what you want to achieve and it will go through your code and make the necessary changes.

Sounds cool right? This must be the end of Software Engineers! Not at all — from my experience, I would describe Claude Code as being like a very energetic puppy; it'll try to do things quickly but it'll make a lot of mistakes and mess along the way. So let's explore what went well and what didn't go well at all.

## What Went Well?

What impresses me most about Claude Code is its speed. No software engineer can read all the code files, make a list of jobs to complete, and add or delete code within a few minutes. Even with the assistance of GitHub Copilot to suggest the code we would like to write, we wouldn't be able to develop at this pace.

I have already documented that Claude produces some stunning UIs (User Interfaces) in this blog post: [Challenge: Build an Insurance Policy Admin System in 2 Days Using AI](_posts/2026-03-25-InsurancePASin2Days.md).

## What Didn't Go Well?

Unfortunately, many things did not go well during my thorough road test:

- **The lies** - I posed a question to Claude Code about whether it was necessary to provide one user with a reference number to give to another, even though the next user cannot search for the reference number or use it whatsoever. I was confidently told the reference number was very important and was used inside my application. When I confronted Claude Code with evidence of its lies, it told me it was sorry and had been overconfident, that it hadn't even checked the code, that I was correct to flag this, and that it had fixed the issue.

- **Spending your usage quota fixing problems it created itself** - This is a very common frustration. Even with a Professional subscription, you're still restricted to a quota and Claude Code will burn through it quickly to fix issues it created within the code. If your quota runs out, it will halt fixing those issues until your quota is refreshed — and sometimes that refresh won't happen for another three hours, leaving you to wait or pick up where it left off. You can switch to a Pay-As-You-Go basis in your Claude settings, but this introduces unpredictable additional costs.

- **Not cleaning up after itself** - On a few occasions Claude Code will identify a bug as some code that it had previously rewritten but not deleted. Just yesterday, when I asked why a feature was not working, it said it was because I was writing to a local database. That same morning I had asked that we migrate out of a local database and into an Azure cloud database. Claude Code sometimes writes new code but leaves the old code behind. Another example was when I asked for a full code review and Claude Code found leftover pieces of code that were no longer referenced.

- **Bad technology advice** - I made it clear to Claude Code from the beginning that my long-term goal was to use Azure Cosmos Database with a C# Web API. It suggested that I use a SQLite database and an Express API and then migrate later to the cloud. I thought it was odd to use a SQL database and later convert to a NoSQL database, but I went along with it for the learning experience. It was a big mistake, because when we did migrate, many original bugs were reproduced in C# and had to be fixed a second time. When I confronted Claude Code about this mistake, it said it didn't recall suggesting those technologies, and denied that they had been the wrong choice given my long-term goals.

- **Code quality issues** - Claude Code does not always follow best practice when writing code. In C# for example, it tried to fix an issue by changing a type to "Object". An experienced developer would know that this is not the correct choice. If some data is text, you would use a "String" datatype — not a generic high-level Object.

- **Trademark infringement** - Claude suggested I call my application FixItFlow and we worked together for months on this basis. Later, when I researched competitors for my app, I found a company providing a similar product called FixFlo. My jaw nearly hit the ground because I had just purchased a domain name for 10 years at a cost of £300! Fortunately, and thanks to the good people at GoDaddy, I was able to get a refund and buy a new domain. When I confronted Claude over this, it said that I'd be lucky if my application was even recognised by the creators of FixFlo, that at worst I'd get a "cease-and-desist letter", and not to worry about it.

## Final Thoughts

In software engineering we have the development "Golden Triangle" of time vs cost vs quality, and we say that in every project we can achieve one of these things at the cost of the others. It could be argued that Claude Code achieves speed, but at the expense of cost — for a Professional subscription — and even more so at the expense of quality.