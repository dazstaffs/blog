---
layout: post
title: "AI Strategy For Financial Services"
date: 2026-11-04
categories: [AI, Insurance]
---

## Introduction

The Bank of England and FCA's [2024 survey of AI in UK financial services](https://www.bankofengland.co.uk/report/2024/artificial-intelligence-in-uk-financial-services-2024) found that 75% of firms are already using AI, and that a third of all use cases are now third-party implementations. Four of the top five risks firms reported were about data: privacy, quality, security and bias.

So most firms are already using AI, more and more of it runs on someone else's platform, and data is what worries them most. Meanwhile Capgemini's [World Property and Casualty Insurance Report 2026](https://www.capgemini.com/news/press-releases/the-moment-of-ai-truth-for-property-casualty-insurance-trailblazers-see-21-higher-revenue-growth-while-broader-industry-lags/) found that only 10% of insurers are successfully scaling AI, and 55% say it's unclear who owns their AI initiatives.

My view is that a workable AI strategy for a financial services firm comes down to three decisions: which high-value processes AI should strengthen, where the models run, and what AI is never allowed to touch. Get those right and the tooling choices become much easier.

---

## Augment the Experts, Don't Replace Them

The business case that starts with headcount reduction is usually the one that stalls. It puts the experts you need on side against the project, and it aims AI at the work where mistakes are most expensive.

A better starting point is to ask where your best people spend time on work that isn't the judgement you hired them for. In insurance that list writes itself:

| Process | Where AI helps | Who stays accountable |
|---|---|---|
| Commercial underwriting | Pulling key facts out of broker submissions, emails and schedules | The underwriter, who still prices and accepts the risk |
| Claims handling | Summarising the file, flagging missing documents, suggesting next steps | The claims handler, who decides and talks to the customer |
| Fraud | Spotting patterns across claims for a human to investigate | The fraud investigator |
| Compliance and complaints | Drafting first responses and finding precedent | The compliance or complaints lead, who signs off |

In every row the expert gets faster and better informed, and the decision stays with a named person. That last column matters to the regulator as much as to your staff: under the Senior Managers and Certification Regime, accountability still sits with people, not systems.

---

## Where the Model Runs Is a Strategic Choice

[Ollama](https://ollama.com) is an open-source tool that lets you run open models such as Llama, Mistral or Qwen on your own servers or laptops, behind your own firewall. For FinTech and insurance firms that changes several conversations at once:

| | Hosted AI service | Local models via Ollama |
|---|---|---|
| Customer data | Leaves your environment, governed by contract | Stays in-house |
| Data residency | Depends on the provider's regions | You decide where it lives |
| Regulator and audit questions | You rely on the vendor's answers | You can show exactly what ran and where |
| Cost | Per use, rises with volume | Mostly fixed hardware and running costs |
| Capability | Access to the most capable models | Smaller models, usually good enough for focused tasks |
| Effort | Vendor runs it | You patch, monitor and test it |

Local isn't automatically better: you take on the operational work, and hosted models are still ahead on complex reasoning. But for high-volume, sensitive work such as summarising claims files that contain medical reports, a local model is often good enough, easier to explain to your risk function and more predictable in cost. Most firms will end up with a mix, using local models for sensitive, repeatable tasks and hosted ones where capability really matters and the data allows it.

---

## A Governance Framework That Gets Used

Governance only works if teams can follow it without waiting months for a committee, so I'd keep it to two parts. The first is a repeatable assessment for every new AI tool, whether it's a vendor product, a copilot feature in software you already use, or something built in-house:

| Area | Questions to answer |
|---|---|
| Data handling | What data goes in, where is it processed and stored, and is it used to train anyone's model? |
| Explainability | Can we explain an output to a customer, an auditor or the FCA? |
| Vendor risk | How financially stable is the supplier, who do they depend on, and does this add to concentration risk? |
| Cost | What does it cost at full volume, not pilot volume? |
| Exit plan | How would we switch it off or move to another provider, and what happens to our data? |

The second is a short, published list of processes AI must never touch. Here is my starting list for an insurer:

- Final decisions to decline a claim or cancel a policy
- Decisions involving customers identified as vulnerable
- Final responses to complaints
- Regulatory attestations and sign-offs by senior managers
- Putting pricing changes live

Writing it down gives teams a clear boundary and the board something concrete to approve, and it fits the FCA's Consumer Duty focus on good customer outcomes. If you operate in the EU, check where your use cases sit under the EU AI Act, which treats some life and health insurance uses as high-risk. Have your compliance team confirm the current position for your markets.

---

## Final Thoughts

AI strategy in financial services isn't about the cleverest model. It's about pointing AI at the right work, keeping sensitive data where you can control it, and being clear about where the line is. Here is a checklist a CTO and COO can work through together:

- **Processes:** Have we named three high-value processes where AI will support our experts, each with an accountable owner?
- **Ownership:** Does each AI initiative have one business owner and one technology owner?
- **Deployment:** For each use case, have we decided between local and hosted models based on the data involved?
- **Assessment:** Does every new AI tool go through the same five-part assessment before it's switched on?
- **Never-touch list:** Have we written the list down, had it approved at board level, and told staff about it?
- **Measurement:** Are we tracking time saved, quality and customer outcomes, rather than just usage?
