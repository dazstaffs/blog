---
layout: post
title: "Troubleshooting Azure Quote Issues"
date: 2026-02-28
categories: [azure]
---

Here is the scenario - you're trying to create a Web App in Azure, possibly in the 'UKSouth' region but you keep getting this Azure Quote error when you press create:

![Image]({{ site.baseurl }}/assets/images/Additional_Quota_Reqd.png)

---

### 1. **The Fix**

A simple fix, change the region to something else, such as 'CanadaCentral' and retry.

### 2. **The Cause**

At first I thought this must be due to problems with my account. Following Azure's own recommendations, I logged a ticket to ask for a bigger quota, but tickets take up to 10 days to be resolved for individuals.

I have a theory that because UKSouth is overcapacity, Azure doesn't allow servers to be created in this region if you're an individual and not a corporation. 

--- 

