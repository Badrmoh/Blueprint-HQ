# 1. Dexter: AI agents for mechanical contractors

##  **TL;DR**

Mechanical contractors struggle to get timely, accurate updates from the field because reporting is slow and still relies on paper. This leads to project delays, late payments, and frustrated clients.

Dexter’s AI agents make it easy to capture field data using voice, images or documents, enrich it with context, and turn it into structured updates for both construction and service work.

### Problem

Completing construction projects on time is notoriously difficult - 75% of construction projects are not done on time - and delays mean financial penalties, strained client relationships, and lost revenue from the next job. The reason for most delays is broken communication between in-field and back office teams.

- **Field reporting is broken.** Many foremen, superintendents and service techs still rely on pen and paper or clunky apps they hate using. This means daily logs and service reports are often late or incomplete.
- **Project managers are flying blind.** Without timely field updates, issues like install errors, weather delays or missing parts go unresolved, delaying schedules and driving up labor costs.
- **Payments are delayed.** Missing reports hold up invoicing and can lead to billing disputes, resulting in cash crunches.
- **Missed documentation = missed revenue.** Change orders, service upsells, and warranty claims fall through the cracks without clear documentation, costing contractors thousands.

### Solution

AI agents that work like a new crew member, no training needed.

- **Voice-powered reporting, built for the field.** Dexter’s voice AI lets foremen and techs log updates just by talking - no typing, clunky apps or forms.
- **Remembers what’s been done, and what’s next.** Dexter tracks past progress and follows up automatically, so nothing slips through the cracks on long installs or repeat service visits.
- **Enriched with knowledge.** Integrated with your ERP and project management tools, Dexter pulls in job info like site details, tasks, and deadlines, so the AI starts with context.
- **Generate structured, client-ready reports.** Create customizable reports with photos, equipment, and job details. Upload past examples to easily create templates, so reports are ready to send to GCs, clients, or accounting.
- **Easily digitize paper documents.** Construction sites still rely on paper for deliveries, timesheets, and more. Dexter’s AI can extract all relevant information, verify it against your project plan, and add it to your ERP.

### Use Cases

- **Daily Logs Agent:** Dexter’s voice AI calls your foreman or super when they leave the site, asks what got done, automatically pulls in weather and project data, and generates the log for them. The completed log is instantly sent to your PM’s inbox.
- **Production Reports Agent:** Log field hours via GPS tracking, pull material data from your ERP, and compare progress to plan. Your foreman or super uses the voice agent to add context, and the agent turns it all into an actionable report for project managers.
- **Service Reports Agent:** Dexter’s voice agent talks to service techs to collect all required information about the job, including parts used and any follow-ups needed. The agent extracts asset data via photos, and generates a full report for customer approval.
- **Invoice Match Agent:** Dexter digitizes delivery slips, purchase orders, and invoices, flags overcharges or missing items, handles follow-ups with suppliers, and syncs clean data to the accounting system.

### My Notes
- Same idea can be brought to many field based reporting scenarios:
	- Construction
	- Warehouses (can be helpful in Auditing?)

---
# Bolna - Voice AI for India
### **The Problem**

In India, phone calls remain the backbone of how businesses operate - from banks chasing loan repayments, to edtech companies qualifying leads, to e-commerce brands confirming deliveries. Millions of such calls happen every day. But the system is broken:

- **20+ Languages, 200+ Accents/Dialects**: Building a team that can handle all is impossible. Calls often switch mid-conversation (Hindi → Hinglish → Gujarati), and only a natural, adaptive AI can follow along and give a personalised experience to each caller.
- **Context-Dependent Requirements**: A delivery driver in Bangalore needs a low-latency, Kannada-capable model with high noise cancellation. A recruitment call to an engineer requires a slower but higher-quality reasoning model. There is no “one model to rule them all,” and integrating and managing 100s of models at scale is an unwanted hassle for businesses.
- **Cost Efficiency at Scale**: In India, every rupee matters. Voice AI must be engineered for efficiency - pre-recorded messages for common utterances, smaller vertical-focused models, and intelligent routing to minimize token usage.

### **The Solution**

Bolna is a **Voice AI Platform** purpose-built for India’s scale, linguistic complexity, and cost sensitivity. We enable enterprises to go live with thousands of concurrent calls in days, not months.

- **Enterprise-grade performance**: Sub-500ms latency, interruption handling, multi-language (10+) and accent (50+) adaptation, fluent in natural multi-language conversations (Hinglish, English + Tamil etc.)
- **India-specific routing**: Bolna automatically picks the optimal model blend for the context, regardless of language, region, or use case.
- **Cost-efficiency engine**: Calls are optimized with pre-recorded inserts, cheaper small models where possible, and routing logic that prioritizes ROI without sacrificing experience.
- **Complete control**: Enterprises define workflows, tone, and intelligence. Bolna handles everything behind the scenes.

Today, Bolna powers **500K+ minutes of calls every month** across BFSI, e-commerce, and recruitment. Customers achieve **higher pickup rates, lower costs, and faster deployments** than with any alternative.

For Indian enterprises, Bolna is not just automation, it is the fastest path to scaling voice operations profitably.

---
#  OnDeck AI

### TL;DR

OnDeck lets you analyze any video, without training a model. Instantly find any event, behaviour, or object without needing any training data.

### The Pain:

Creating vision models can take months of engineering time: collecting training data, training, then deployment.  Worse yet:

- it’s often impossible to get enough data for a specific task, and
- even the best cv models struggle to generalize across diverse camera setups, workflows and environments.

### Our Magic:

To overcome these blockers, we bet early on the power of VLMs and built a vision engine that can generalize across any task and doesn’t need any training data. We **published a NeurIPS workshop paper** showing our new methods with VLMs beat traditional CV even at niche tasks.

Why this is good:

- We never train on customer data, unlocking sensitive use cases.
- Deploy instantly and skip months of R&D.
- Identify things that have never been seen before.
- Unlike traditional cv, OnDeck can **_understand_** qualitative behaviour and sequences of events.

This summer we’ve analyzed thousands of hours of footage across:

- Fleets of Autonomous Surface Vessels
- Robotics Research
- Security cameras
- Behaviour analysis for port monitoring
- Off-shore oil & gas monitoring

### My Notes
- The same idea can be used for specific tasks using VLMs
	- maybe deepfake detection
	- technician assistant
- http://nvidia.com/en-us/glossary/vision-language-models/
---

# RamAIm

RamAIn is your real-life Jarvis that works out-of-the-box on your favorite applications including WhatsApp Desktop, Outlook and more. Just tell it what to do sit back and watch it work just like you, intelligently simulating mouse and keyboard clicks to achieve your goals. Current CUAs all follow the same decision loop: screenshot, VLM, decision, repeat. This is expensive, unreliable and slow. We build infrastructure to pre-train CUAs on specific interfaces allowing them to intelligently use the computer super-duper fast.

### My Notes
- It is basically a collection of Computer-Use Agents
- Even Computers can now be operated more efficiently using AI and CUAs
- Other use cases:
	- QS Agents for web apps
	- Industrial OS that doesnt offer Integration neither API
- https://ramain.ai/
- https://github.com/trycua/cua
---

# Sarah AI

Sarah AI is building the AI-native operating system for consumer goods brands—an autonomous supply-chain brain that replaces legacy ERPs and actually runs the business. Founded by Chris (2x Founder; ex-CEO at Better Nature; Forbes 30U30) and Dirk (ex-Google Data, Analytics & AI Lead), we’re backed by YC (W26). In our first month full-time, we’ve raised $1.6M and secured rapid commercial traction with 15 design partners and a growing pipeline of 30+ brands. Our mission is bold: give CPG brands completely hands-free supply chains that run themselves through Sarah, their AI ops assistant. We’re now growing a small, world-class team of builders excited to reinvent how physical goods companies operate—end-to-end, autonomous, and AI-first. If you want to work on hard problems, ship fast, and define the future of autonomous operations, you’ll feel right at home here.

### My Notes
- 