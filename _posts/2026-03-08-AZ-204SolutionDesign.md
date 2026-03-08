---
layout: post
title: "AZ-204 Microsoft Certified Azure Associate Developer - My Solution Design"
date: 2026-03-08
categories: [Azure]
---

I have three goals for March/April. The first is to find a new job, the second is to pass exam AZ-204: Microsoft Certified Azure Associate Developer and the third is to produce more articles for my blog. 

With this in-mind, developing an Azure solution that helps me customise my CV against a job description and utilises all the technologies in the AZ-204 exam curriculum, will assist with these goals. It will certainly lead to many blog posts.

In this blog post, I will start by looking at high-level architecture for this solution. 

---

## High-Level Architecture ##

The first thing that is important to recognise, when designing a high-level architecture is that I am trying to use all the technologies on the AZ-204 curriculum. Therefore, some design choice, may not be the best technologies choices. SQL Server, for example is a technology that I have worked-with for my entire career but doesn't feature on the AZ-204 exam. Azure Static Web Apps(SWAs), are also not featured on the AZ-204 exam but are a technology I would use to host my user interface, because of the way they are globally distributed like a Content Delivery Network, highly secure and in many scenarios, a cost-effective way to host a JavaScript-based front-end. 

With the above design considerations factored in, here is a high-level design. 

![Image]({{ site.baseurl }}/assets/images/AZ204ArchitectureDesign.png)

---

## Design Notes ##

This first draft will evolve over-time as I add more Azure PaaS offerings into the design. This design doesn't cover the three pillars of observability, idempotence, scalability, security or design patterns, but as I cover each individual phase in other blog posts, I will add the low-level design elements there.

---

## Final Thoughts ##

This wraps the first blog post in a series of posts. I will enjoy the process and learning opportunities that this solution will bring. Join me in the next post, where we will build a front-end/user interface.

What do you think about my initial design? I'm always open to feedback, so please do get in-touch via LinkedIn, Email, etc. Links can be found on my contact page.



 



