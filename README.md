# AIFA-AI-Feedback-Agents
🧠 Overview

AIFA (AI Feedback Agents) is an intelligent Multi-Agent System (MAS) built using the JADE framework.
The goal of the system is to automatically collect, analyze, and summarize user feedback across three essential quality dimensions:

Speed

Accuracy

User Experience (UX)

Instead of manually processing surveys or dispersed feedback, AIFA provides an automated, agent-based pipeline that generates a complete performance summary for any AI-enabled service.

🏗️ System Architecture

The system consists of five autonomous agents, each responsible for a specific task:

1️⃣ FeedbackSourceAgent

Collects user ratings (Java Swing interface)

Sends INFORM messages to analytical agents

Notifies the DecisionAgent when feedback entry is complete

2️⃣ SpeedFeedbackAgent

Receives speed-related ratings

Stores values and returns the average upon request

3️⃣ AccuracyFeedbackAgent

Handles accuracy rating collection and aggregation

4️⃣ UXFeedbackAgent

Processes UX ratings and provides evaluation summaries

5️⃣ DecisionAgent

Coordinates the entire system

Sends REQUEST messages to analytical agents

Aggregates averages from all agents

Updates the dashboard and generates the final performance report

🔄 Communication Protocol (FIPA-ACL)
Protocol	Performatives	Purpose
Rating Submission	INFORM	Send user ratings to analytical agents
Feedback Completion	INFORM	Notify DecisionAgent when user finishes
Report Request	REQUEST → INFORM	Request & receive averages from analytical agents

The system fully complies with FIPA-ACL messaging standards for agent-to-agent communication.

🧪 Test Scenarios & Results
Scenario 1 – Balanced Feedback

Input: 3 moderate ratings (3/5 each)

Output:

Speed: 3.00

Accuracy: 3.00

UX: 3.00

Overall: 3.00
📊 Represents balanced system performance

Scenario 2 – Mostly Negative Feedback

Input: 80% negative ratings

Output:

Speed: 2.67

Accuracy: 3.00

UX: 2.67

Overall: 2.78
📉 Indicates poor service trends

Scenario 3 – High UX, Low Speed

Input: High UX, low speed, moderate accuracy

Output:

Speed: 1.67

Accuracy: 3.00

UX: 4.67

Overall: 3.11
📌 Highlights bottlenecks in speed performance

🖥️ Dashboard & Visualization

The system includes:

DashboardUI – displays live metrics

DashboardServer – exposes values via a lightweight HTTP JSON API

ReportStore – shared structure for storing performance data

Users can visualize results immediately after feedback submission.

🧩 Technologies Used

JADE Framework (Multi-Agent Systems)

Java (Swing & AWT)

FIPA-ACL Messaging

Embedded HTTP Server

JSON Metrics API

🎯 Purpose of the System

AIFA helps:

AI service platforms

Customer experience teams

Startups and SaaS companies

Government & enterprise tech units

…to automatically evaluate service quality and detect issues early using Multi-Agent intelligence.

🚀 Future Enhancements

Integrating NLP sentiment analysis

Adding a web-based dashboard

Supporting more rating categories

Storing results in a database

Real-time alerting for low performance

👥 Contributors

Wasan Alomar

Shahad Altamimi

Rama Alotaibi

Ghaida Alanazi

Shahad Alobaid
