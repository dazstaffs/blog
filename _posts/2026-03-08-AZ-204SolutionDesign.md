---
layout: post
title: "AZ-204 Azure Associate Developer Solution - Part 1"
date: 2026-03-08
categories: [Azure]
---

I have three goals for March and April. The first is to find a new job, the second is to pass the AZ-204: Microsoft Certified Azure Developer Associate exam, and the third is to publish more articles on my blog.

With these goals in mind, developing an Azure-based solution that helps customise my CV against a job description while also utilising technologies covered in the AZ-204 exam curriculum, would be many birds with one stone. It will also provide plenty of opportunities for future blog posts.

In this article, I will begin by exploring the high-level architecture for this solution.

---

## High-Level Architecture

When designing a high-level architecture for this project, an important consideration is that I am intentionally trying to incorporate technologies from the AZ-204 curriculum. As a result, some design decisions may not necessarily represent the technologies I would choose in a typical production environment.

For example, SQL Server is a technology I have worked with throughout my career, but it does not feature prominently in the AZ-204 exam. Instead, other Azure-native data services are emphasised.

Similarly, Azure Static Web Apps (SWA) is not explicitly covered in the AZ-204 curriculum. However, it is a service I would normally use to host the user interface because it provides global distribution similar to a Content Delivery Network, strong built-in security, and is often a cost-effective solution for hosting JavaScript-based front-end applications.

Taking these considerations into account, the following diagram shows the initial high-level architecture for the solution.

![Image]({{ site.baseurl }}/assets/images/AZ204ArchitectureDesign.png)

---

## Design Notes

This first draft of the architecture will evolve over time as I incorporate additional Azure Platform-as-a-Service (PaaS) offerings into the design.

At this stage, the architecture does not yet address several important architectural concerns such as:

- observability  
- idempotency  
- scalability  
- security  
- architectural design patterns  

As the solution develops and I cover each phase in future blog posts, I will introduce these lower-level design considerations in more detail.

---

## Final Thoughts

This concludes the first post in what will become a series documenting the development of this solution.

I am looking forward to the learning opportunities this project will provide and to sharing that journey through future blog posts. In the next post, I will begin building the front-end user interface.

If you have any thoughts on this initial design, I would welcome your feedback. Please feel free to get in touch via LinkedIn, email, or any of the other channels listed on my contact page.
 



