---
layout: post
title: "AI Strategy For Financial Services"
date: 2026-11-04
categories: [AI, Insurance]
---

## Introduction

The Cambridge Centre for Alternative Finance's [2026 Global AI in Financial Services Report](https://www.jbs.cam.ac.uk/faculty-research/centres/alternative-finance/publications/2026-global-ai-in-financial-services-report/), published in April, found that 81% of the financial services companies it surveyed are adopting AI at some level. The two risks those companies worried about most were data privacy (74%) and hallucinations, meaning confident but wrong answers (70%). Loss of human oversight was also high on the list, at 55%.

Those three worries are where an AI strategy should start. My view is that it comes down to four decisions: which high-value processes AI should strengthen, how each process is redesigned around AI, where the models run, and what AI is never allowed to touch.

---

## Augment the Experts, Don't Replace Them

The business case that starts with headcount reduction is usually the one that stalls. It turns the experts you need against the project, and it aims AI at the work where mistakes are most expensive. A better question is where your best people spend time on work that isn't the judgement you hired them for. In insurance that list writes itself:

| Process | Where AI helps | Who stays accountable |
|---|---|---|
| Commercial underwriting | Pulling key facts out of broker submissions, emails and schedules | The underwriter, who still prices and accepts the risk |
| Claims handling | Summarising the file, flagging missing documents, suggesting next steps | The claims handler, who decides and talks to the customer |
| Fraud | Spotting patterns across claims for a human to investigate | The fraud investigator |
| Compliance and complaints | Drafting first responses and finding precedent | The compliance or complaints lead, who signs off |

In every row the expert gets faster and better informed, and the decision stays with a named person. Under the Senior Managers and Certification Regime, that's where the regulator expects accountability to sit.

---

## Design the Process With AI in Mind

Picking the process is only half the job. Dropping AI into one step of an existing process usually just moves the bottleneck, so decide up front which steps the AI does, how its output gets checked, and when a person steps in. A handful of design patterns cover most cases:

| Pattern | How it works | Insurance example |
|---|---|---|
| Prompt chaining | The task is split into small steps, each with its own prompt, and each output feeds the next step | Extract data from a broker submission, check it against underwriting appetite, then draft a referral note |
| AI evaluating AI | A second model checks the first model's output against the source documents or a set of rules | A checker confirms every figure in a claims summary actually appears in the claim file |
| Human-in-the-loop | A person approves every AI output before it's used | A claims handler approves each settlement recommendation |
| Human-on-the-loop | AI handles routine cases, and a person steps in when confidence is low or something looks wrong | A chatbot answers policy questions and hands over when a customer is frustrated |

Prompt chaining is the pattern I'd reach for first: each step is small enough to test, and when something goes wrong you can see which step failed, so hallucinations are easier to catch.

So is it okay for AI to evaluate AI? I think so, as long as the checker catches problems and sends them to a person rather than signing off decisions that matter. The Financial Stability Board's [final report on responsible AI adoption](https://www.fsb.org/2026/10/fsb-finalises-sound-practices-for-the-responsible-adoption-of-artificial-intelligence-ai/), published in October, accepts that people can't watch every AI decision once use scales, and supports AI monitoring AI provided the monitor is independent of the system it checks. The same report gives approving a health insurance claim as a case where a person should approve every decision, because accuracy matters more than speed.

---

## Where the Model Runs Is a Strategic Choice

Data privacy topped the Cambridge list of worries, and where your models run decides a lot of it. [Ollama](https://ollama.com) is an open-source tool that lets you run open models such as Llama, Mistral or Qwen on your own servers, behind your own firewall. For FinTech and insurance companies that changes several conversations at once:

| | Hosted AI service | Local models via Ollama |
|---|---|---|
| Customer data | Sent to the provider's servers, and how it's stored and used depends on your contract with them | Never leaves your own servers |
| Data residency | Depends on the provider's regions | You decide where it lives |
| Regulator and audit questions | You rely on the vendor's answers | You can show exactly what ran and where |
| Cost | Per use, rises with volume | Mostly fixed hardware and running costs |
| Capability | Access to the most capable models | Smaller models, usually good enough for focused tasks |
| Effort | Vendor runs it | You patch, monitor and test it |

Local isn't automatically better, and hosted models are still ahead on complex reasoning. But for sensitive, high-volume work such as summarising claims files that contain medical reports, a local model is often good enough and far easier to explain to your risk function. Most companies will end up with a mix.

---

## A Governance Framework That Gets Used

Governance only works if teams can follow it, so I'd keep it to two parts. The first is a repeatable assessment for every new AI tool, including copilot features switched on in software you already use:

| Area | Questions to answer |
|---|---|
| Data handling | What data goes in, where is it processed and stored, and is it used to train anyone's model? |
| Explainability | Can we explain an output to a customer, an auditor or the FCA? |
| Vendor risk | How financially stable is the supplier, who do they depend on, and are we relying too heavily on one provider? |
| Cost | What does it cost at full volume, not pilot volume? |
| Exit plan | How would we switch it off or move to another provider, and what happens to our data? |

The second is a short, published list of processes AI must never touch. Here is my starting list for an insurer:

- Final decisions to decline a claim or cancel a policy
- Decisions involving customers identified as vulnerable
- Final responses to complaints
- Regulatory attestations and sign-offs by senior managers
- Putting pricing changes live

Writing it down gives teams a clear boundary and fits the FCA's Consumer Duty focus on good customer outcomes. If you operate in the EU, check where your use cases sit under the EU AI Act, which treats some life and health insurance uses as high-risk.

---

## Final Thoughts

AI strategy in financial services isn't about the cleverest model. Here is a checklist a CTO and COO can work through together:

- **Processes:** Have we named three high-value processes where AI will support our experts, each with an accountable owner?
- **Design:** For each process, have we chosen how AI output gets checked, and is any checking independent of the model it checks?
- **Deployment:** For each use case, have we decided between local and hosted models based on the data involved?
- **Assessment:** Does every new AI tool go through the same five-part assessment before it's switched on?
- **Never-touch list:** Have we written the list down, had it approved at board level, and told staff about it?
- **Measurement:** Are we tracking time saved, quality and customer outcomes, rather than just usage?
