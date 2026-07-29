<div align="center">

# 🎂 Bakers Corner — AI Customer Support Agent

### An intelligent, 24/7 AI-powered customer support agent for a NYC-based bakery
### Built with n8n, OpenAI GPT-4o-mini, Supabase (pgvector), and Slack

<br>

![Status](https://img.shields.io/badge/Status-Live%20Demo-success?style=for-the-badge)
![n8n](https://img.shields.io/badge/n8n-Workflow-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o--mini-412991?style=for-the-badge&logo=openai&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-pgvector-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Slack](https://img.shields.io/badge/Slack-Integration-4A154B?style=for-the-badge&logo=slack&logoColor=white)

<br>

### 🎥 [**Watch the Live Demo (60 seconds)**](https://www.loom.com/share/e5ed82c333fd42259b9225f4b13438fc)

<a href="https://www.loom.com/share/e5ed82c333fd42259b9225f4b13438fc">
  <img src="https://cdn.loom.com/sessions/thumbnails/e5ed82c333fd42259b9225f4b13438fc-with-play.gif" width="600" alt="Demo Video">
</a>

</div>

---

## 📖 Overview

**Bakers Corner AI Agent** is a production-ready AI customer support assistant designed for small-to-medium businesses. Built as a portfolio showcase by **Daynix Studio**, it demonstrates how a modern RAG (Retrieval-Augmented Generation) architecture can automate 90%+ of customer inquiries — from pricing questions to delivery details — while keeping the business owner informed of every conversation via Slack.

The demo business is **Bakers Corner**, a fictional custom cake shop in New York City. The underlying architecture is completely **channel-agnostic** and **reusable across any industry** — replace the knowledge base and you have an agent for a salon, clinic, boutique, restaurant, or service business in under a day.

<br>

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🤖 **24/7 Automated Support** | Instant, natural-language responses to customer questions — no waiting, no missed inquiries. |
| 📚 **RAG-Powered Accuracy** | Every reply is grounded in the business's real knowledge base — zero hallucinations. |
| 🧠 **Semantic Search** | pgvector-powered similarity search finds the most relevant answers from 27+ FAQs across 6 categories. |
| 💬 **Conversation Memory** | Persistent conversation history per user, stored in Supabase for context-aware follow-ups. |
| 🔔 **Real-Time Slack Alerts** | Every conversation is instantly forwarded to the shop owner's Slack channel for full visibility. |
| 🔌 **Channel-Agnostic** | Deploy on web chat, WhatsApp, Instagram, or Messenger — same brain, any front-end. |
| 🎨 **Easily Customizable** | Swap the knowledge base and branding — deploy for any small business in 1-2 days. |


<br>

## 🛠️ Tech Stack

<table>
<tr>
  <td width="30%"><b>Layer</b></td>
  <td width="30%"><b>Technology</b></td>
  <td width="40%"><b>Purpose</b></td>
</tr>
<tr>
  <td>Orchestration</td>
  <td>n8n Cloud</td>
  <td>Workflow engine connecting all services</td>
</tr>
<tr>
  <td>Language Model</td>
  <td>OpenAI GPT-4o-mini</td>
  <td>Natural, contextual response generation</td>
</tr>
<tr>
  <td>Embeddings</td>
  <td>OpenAI text-embedding-3-small</td>
  <td>Convert text to vectors for semantic search</td>
</tr>
<tr>
  <td>Vector Database</td>
  <td>Supabase + pgvector</td>
  <td>Store & search knowledge base semantically</td>
</tr>
<tr>
  <td>Persistence</td>
  <td>Supabase (PostgreSQL)</td>
  <td>Store conversation history per user</td>
</tr>
<tr>
  <td>Notifications</td>
  <td>Slack Webhooks</td>
  <td>Real-time owner alerts for every conversation</td>
</tr>
</table>

<br>

## 📸 Screenshots

<div align="center">

### n8n Workflow Overview
<img src="screenshots/01-n8n-workflow.png" width="800" alt="n8n Workflow">

### Supabase Knowledge Base (27 FAQs Embedded)
<img src="screenshots/02-supabase-knowledge-base.png" width="800" alt="Knowledge Base">

### Live Chat Demo
<img src="screenshots/05-chat-demo.png" width="600" alt="Chat Demo">

### Real-Time Slack Notification
<img src="screenshots/04-slack-notification.png" width="600" alt="Slack Alert">

### Conversation History (Persistent Memory)
<img src="screenshots/03-supabase-conversations.png" width="800" alt="Conversations Table">

</div>

<br>

## 📂 Repository Contents


<br>

## 🚀 How to Deploy This Agent

### Prerequisites
- n8n Cloud account (or self-hosted n8n)
- OpenAI API key with $5+ credit
- Supabase project (free tier works)
- Slack workspace with an incoming webhook

### Setup Steps

1. **Provision Supabase**
   - Create a new project
   - Enable the `pgvector` extension
   - Run `database_schema.sql` in the SQL Editor to create tables and the vector search RPC

2. **Configure n8n Credentials**
   - Add OpenAI credential
   - Add Supabase credential (URL + service_role key)

3. **Import Workflows**
   - Import `KB_Loader.json` → run once to populate the knowledge base
   - Import `Bakers_Corner_Agent.json` → your live agent

4. **Set the Slack Webhook**
   - In the main workflow, open the Slack node
   - Paste your own incoming webhook URL

5. **Activate & Test**
   - Toggle the main workflow to **Active**
   - Use the built-in Chat trigger URL to test — or embed it in your website

<br>

## 💡 Real-World Use Cases

This architecture is production-ready for any business that gets repetitive customer inquiries:

- 🎂 **Bakeries & Cafes** — menu, pricing, custom orders, delivery
- 💇 **Salons & Spas** — services, appointments, pricing, availability
- 🏥 **Clinics & Dental Offices** — hours, insurance, appointment booking
- 🛍️ **E-Commerce Stores** — product info, shipping, returns
- 🏨 **Hotels & Rentals** — availability, amenities, booking
- 🎓 **Coaches & Consultants** — services, packages, scheduling

<br>

## 👨‍💻 About the Developer

<table>
<tr>
<td width="30%" align="center">
  <b>Tayyab Nazir</b><br>
  <i>Founder — Daynix Studio</i><br>
  AI Automation Consultant<br>
  Based in Pakistan 🇵🇰<br>
  Serving clients globally 🌍
</td>
<td width="70%">
  I build AI agents and automation systems for businesses that want to scale without scaling their support team. My work spans customer support agents, lead qualification bots, appointment schedulers, and full-stack AI integrations across n8n, OpenAI, Anthropic Claude, Supabase, and Vapi.
  <br><br>
  Prior to focusing on AI automation, I've built and shipped multiple Android apps live on Google Play, giving me a full-cycle development background from mobile to backend to AI orchestration.
</td>
</tr>
</table>

<br>

## 🏢 About Daynix Studio

**Daynix Studio** is an AI automation studio focused on building custom AI agents, chatbots, and workflow automations for small and medium businesses worldwide. We specialize in:

- 🤖 Custom AI Agents (Customer Support, Lead Qualification, Sales)
- 🔗 Business Process Automation (n8n, Zapier, Make)
- 💬 WhatsApp, Instagram & Web Chat Integrations
- 🧠 RAG Systems & Knowledge Base Deployment
- 🎯 Voice AI Agents (Vapi, Retell)

Every agent we deliver is **built to scale with your business** — modular, well-documented, and easy to maintain.

<br>

## 📞 Get in Touch

<div align="center">

Interested in a similar AI agent for your business? Let's talk.

🌐 **Website:** [daynixstudio.com](https://daynixstudio.com)
✉️ **Email:** [info.daynixstudio@gmail.com](mailto:info.daynixstudio@gmail.com)
🎥 **Live Demo:** [Watch on Loom](https://www.loom.com/share/e5ed82c333fd42259b9225f4b13438fc)

<br>

**⭐ If this project inspires or helps you, please give it a star.**

</div>

<br>

---

<div align="center">
  <sub>Built with ❤️ by <a href="https://daynixstudio.com">Daynix Studio</a> · Portfolio Project 2026</sub>
</div>

<br>

## 🏗️ Architecture
