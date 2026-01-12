# Social-to-Lead Agent

This project is a conversational AI agent built for a fictional SaaS product called AutoStream.  
AutoStream helps content creators automate video editing.

The agent chats with users, answers product and pricing questions using a local knowledge base (RAG), identifies users who want to sign up, collects their details, and captures them as leads.

---

##  Project Purpose

The goal of this project is to demonstrate how an AI agent can:

- Talk to users naturally  
- Answer pricing and product questions accurately  
- Detect high-intent users  
- Maintain conversation state across multiple turns  
- Capture lead information safely using tool execution  

This simulates a real-world customer support and sales assistant.

---

 Key Capabilities

 1. Intent Detection
The agent identifies the user’s intent at each step of the conversation:
- Casual conversation  
- Pricing or product inquiry  
- High-intent (ready to sign up)

High-intent detection is prioritized so the agent can switch into lead capture mode at the correct time.

--

 2. RAG-Based Knowledge Retrieval
The agent answers pricing and product questions using a *local knowledge base, which simulates a **Retrieval-Augmented Generation (RAG)* workflow.

When a user asks about pricing:
- Relevant product information is retrieved from predefined knowledge
- The agent responds using this retrieved data

This ensures accurate, consistent answers without hallucination and without relying on external APIs.

---

3. Stateful Conversation Management
The agent maintains state across multiple conversation turns, including:
- Current conversation stage  
- Detected intent  
- Collected user details (name, email, platform)

A two-stage flow is used:
- Conversation stage (Q&A and intent detection)  
- Lead capture stage (structured data collection)

This prevents the conversation from reverting back to pricing once the user shows sign-up intent.

---

 4. Tool Execution – Lead Capture
Once a user is identified as high-intent, the agent collects:
1. Name  
2. Email  
3. Content creation platform  

After collecting all required information, the agent executes a mock backend tool:

```python
mock_lead_capture(name, email, platform)


How to Run the Project

Open the Jupyter Notebook
Run all cells from top to bottom
Start chatting with the agent in the final cell
Type exit to stop the conversation

Demo Video

[LINK-](https://youtu.be/aWyW7K1Ee6o)

A short demo video demonstrates:
Pricing query handling using RAG
High-intent detection
Multi-step lead information collection
Successful tool execution
(The demo video link is included in this repository.)

Tools & Technologies Used

Python
Jupyter Notebook
Rule-based intent detection
Local RAG-style knowledge retrieval
Stateful agent logic

 Why This Project Is Useful

This project demonstrates:
Clear conversational flow
Explicit state management
Controlled and safe tool execution
Practical application of RAG and agentic design

The same design can be extended to real-world deployments such as WhatsApp or web chat using webhooks.
