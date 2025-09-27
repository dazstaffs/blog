---
layout: post
title: "Data Driven Decisions - The value in data-driven decisions, the data I collect and how I use it"
date: 2025-09-27
categories: [data, leadership]
---

"...most conference rooms at Google have two projectors. One of them is for video-conferencing with other offices or for projecting meeting notes. The other is for data." says Eric Schmidt in the great book "How Google Works". He goes on to say "We don't seek to convince by saying 'I think.' We convince by saying 'Let me show you.'"

This quote has always stuck with me throughout my career so far and I have found that out of all of the sectors that I've worked in, which includes Pharma, Manufacturing, etc, insurance has been the worst industry for IT decisions based on opinions than data. This week in particular has stood out for me as being one week, where for two days in a row, I have had to step in and say, "Well actually, this data suggests this is not true" and personally I hate to have to say this; I'd much rather data was presented for every decision made, because I certainly will not make blind decisions.

In this article I'm going to outline how I use data to make decisions and why.

---

## Application Usage Data

For me this is an important one. This week someone said that our business stakeholders want to move all of their data out of a system and into an Excel spreadsheet and that my manager had agreed the decision so let's not argue about if it's a good idea. I was able to bring Power BI up on-screen and say, this system has been used 1552 times last month by 8 different people. Immediately, the reply was, "okay maybe Excel would not be a viable solution". A second good example of the importance, is how another person told me that another system was used once a month, so let's provide a cut of the data, once a month. Again, I could show usage data that suggests that's not true and a daily cut of data would be a better idea.

This goes way beyond if systems would be more efficient in Excel and about design decisions, as mentioned above. If a stakeholder asks for a new feature in a piece of software, how do you measure if that feature was a success without data. If the point of a new feature is to make a manual task take 10 mins vs a day, why would you not measure how long it takes to complete the task before and after the new feature is released, perhaps you need to measure how often that feature is used and if it's not being used, why not? In the software engineering world, we should never underestimate usage data for every system that we build.

## Team Mood

I collect data on my team's mood in one of two ways. Firstly, in our weekly check-in, I will ask them how they feel about work on a scale of 1 to 4, where 1 is fantastic and 4 is terrible. If someone scores a 3 or higher, I will ask them why they feel this way and what I can do to make things better for them. I also use this weekly score to gauge how hard I am pushing the team. If I'm asking a developer to do more work and their scores are increasing, I will then assess if I'm overloading that developer.

The other metrics I take from each team member, is within our quarterly retrospective where I ask them to score out of ten, how they feel about clarity, energy, psychological safety, work-life balance, confidence and efficiency at work. From this data I look for trends and always hope that for each quarter, our graphs are moving in a positive direction, because this shows my progress as a leader.

## Service Management Metrics

Service Management data can be broken down into two areas. Firstly, I collect data for incidents and requests that enter my ServiceNow queue. In our monthly reporting meeting, I use this data to advise if my tickets were completed within SLA, which types of requests we are getting, which systems are causing the most incidents and thus might require some investment and if any continuous improvement is reducing our ticket numbers (and I'm pleased to see that my Continuous Improvement initiatives really are paying off because I know for some applications, ticket numbers have fallen to single digits annually).

Secondly, I collect data for all incidents and requests that my team members have logged. This data has led to many difficult questions between myself and our Service Management team such as, how does a ticket stay open and active for 54 days and within SLA, why does this ServiceNow queue have no assignees in it, why is this ticket pending approval from someone who no longer works here, why is it that this person never approves any tickets unless I chase them and many other insights which, if fixed, ultimately improves the overall performance of my team. I scour this data at least once a day and do not expect my team members to have to chase me, to get things done.

## Azure DevOps Metrics

Metrics from Azure DevOps are crucial for managing a large team of 21 engineers. As the head of software engineering, I'm unable to attend 8 daily stand-ups but I need to know how each developer is performing, how a project is progressing, if someone is currently blocked and why, which products have the biggest backlog and may require more resources, which products have a small backlog and thus less resources, feature estimates vs actual delivery times, cycle times, lead times, bugs vs tasks, which teams are working in an agile way vs a waterfall way, why some teams seem to create tasks for testing than use a lane on the KANBAN board, which developers need agile training and underlying all of this data, is a date-picker that allows me to analyse everything over a selected period of time. I also will go into my weekly check-in and ask developers to talk over what we're seeing in Power BI from the last week and also why we're not seeing many tasks for some other developers.

## Desk Bookings

I used to capture desk booking data from Condeco but soon gave up on this, because if someone doesn't book a desk and they just turn-up and sit in a free space, the data is inaccurate. I then tried getting access to building access logs but was denied.

## Workday Data

I put in a request to get access to my team's holiday bookings and yearly goal data, to try to identify any trends but our HR team asked me for some budget to work on this and I didn't have a budget for any of the data collection listed above, so this request went nowhere.

---

## Final Thoughts

This is just some of the data that I regularly collect to be the best head of software engineering that I can be and to ensure that any decisions around my products and team, are well founded. I hope you found this article a good read and that you can see the importance of data collection. I certainly feel enlightened by collecting and analysing data across many areas of my team and I owe thanks, to Eric Schmidt and Jonathan Rosenberg, the writers of "How Google Works", that I recommend all leaders read at least once.

Thanks for reading and have a good weekend!

Darren
