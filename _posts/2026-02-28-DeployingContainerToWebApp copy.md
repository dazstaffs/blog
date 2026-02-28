---
layout: post
title: "Troubleshooting Azure Container to Webapp Load Issues"
date: 2026-02-28
categories: [azure]
---

Here is the scenario - you've created an Azure Container Registry, you've created a web application in Visual Studios, you've deployed this application to your registry and you want to deploy from the registry to an Azure Web App because of all the lovely benefits it brings. Upon deploying your application, the web page doesn't load, it spins around and around and you think you've made a mistake somewhere along the way. You've followed all the steps correctly, Azure Co-pilot sends you in loops and to webpages that are completely irrelevant and before you know it, you've wasted 8 hours of your life troubleshooting the problem.

Well in this post I am going to provide you with the fix and explain why this is happening. 

---

### 1. **The Fix**

For those who have no interest in understanding the why, let's jump to the fix. Open your Azure Web Application > Settings > Environment Variables > Add. Name = "WEBSITES_PORT", value is whatever port you bound the application to in the docker file. If you created the web app using Visual Studios, it's probably 8080 and 8081, but as Webapps can only support one port, add 8080 to the value. 

![Image]({{ site.baseurl }}/assets/images/8080PortBindinginVS.png)

![Image]({{ site.baseurl }}/assets/images/WEBSITES_PORT.png)

Apply the changes. Refresh the page and voila, it works:

![Image]({{ site.baseurl }}/assets/images/WebApp3_Works.png)

### 2. **The Cause**

Two causes for this problem. Firstly Azure Web Apps like to listen on just one port number and secondly, around August 2025, Microsoft added new functionality to Azure Web Apps which made manual port binds irrelevant: 

![Image]({{ site.baseurl }}/assets/images/AzurePortBindingsNotWorking.png)

--- 

## Final Thoughts

It is recommend to create Azure Container Applications to do multi-port bindings. If you create an Azure Container App from Visual Studios, everything should work from the offset, although knowing Azure there are many things to trip you along the way.

