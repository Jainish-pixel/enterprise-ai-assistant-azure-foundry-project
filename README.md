🚀 Enterprise AI Assistant using RAG, MCP & Microsoft Azure

An intelligent enterprise AI assistant built using Microsoft Azure AI Foundry, Foundry IQ, RAG, Azure AI Search, MCP and Azure Functions.

The system enables employees to ask questions from enterprise knowledge sources and perform actions such as creating IT tickets, retrieving ticket information and submitting leave requests through AI-powered tools.

📌 Project Overview

Organizations maintain large amounts of internal information such as HR policies, IT documentation, employee guidelines and operational procedures.

Finding this information manually can be time-consuming.

This project provides an AI-powered Enterprise Knowledge Assistant that combines:

🤖 Microsoft Azure AI Foundry

🧠 AI Agents

📚 Foundry IQ Knowledge Base

🔎 Azure AI Search

🔗 Retrieval-Augmented Generation (RAG)

🛠️ Model Context Protocol (MCP)

⚡ Azure Functions

🚀 FastAPI

🌐 Web-based AI Chat Interface

The assistant can both retrieve enterprise knowledge and execute enterprise actions.

🏗️ System Architecture

                         ┌──────────────────────┐
                         │    Employee / User   │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │    Web Application   │
                         │   FastAPI + Frontend │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │ Microsoft Azure AI   │
                         │       Foundry        │
                         │      AI Agent        │
                         └──────────┬───────────┘
                                    │
                  ┌─────────────────┴─────────────────┐
                  │                                   │
                  ▼                                   ▼
       ┌──────────────────────┐            ┌──────────────────────┐
       │   Foundry IQ         │            │     MCP Server       │
       │   Knowledge Base     │            │   Azure Functions    │
       └──────────┬───────────┘            └──────────┬───────────┘
                  │                                   │
                  ▼                                   ▼
       ┌──────────────────────┐            ┌──────────────────────┐
       │   Azure AI Search    │            │    MCP Tools         │
       │   Document Retrieval │            │                      │
       └──────────┬───────────┘            │ • Create IT Ticket  │
                  │                        │ • Get IT Ticket     │
                  ▼                        │ • Leave Request      │
       ┌──────────────────────┐            └──────────────────────┘
       │ Enterprise Documents │
       │                      │
       │ • HR Policies        │
       │ • IT Documentation   │
       │ • Company Guidelines │
       └──────────────────────┘
🔄 Complete Workflow
                    USER
                      │
                      ▼
              Web Application
                      │
                      ▼
              Azure AI Foundry
                   AI Agent
                      │
             ┌────────┴────────┐
             │                 │
             ▼                 ▼
       Knowledge Base       MCP Server
             │                 │
             ▼                 ▼
      Azure AI Search      Azure Functions
             │                 │
             ▼                 ├───────────────┐
     Relevant Documents       │               │
             │                ▼               ▼
             │         Create Ticket     Get Ticket
             │
             │                │
             │                ▼
             │         Leave Request
             │
             └────────┬───────────────┘
                      │
                      ▼
                AI Agent
                      │
                      ▼
               Final Response
                      │
                      ▼
                     USER
🧠 RAG Workflow

The project uses Retrieval-Augmented Generation (RAG) to provide responses based on enterprise documents.

User Question
      │
      ▼
Query Processing
      │
      ▼
Foundry IQ Knowledge Base
      │
      ▼
Azure AI Search
      │
      ▼
Relevant Documents
      │
      ▼
Retrieved Context
      │
      ▼
AI Model
      │
      ▼
Grounded Response

This allows the assistant to use enterprise-specific information instead of relying only on general model knowledge.

📚 Knowledge Base

The enterprise Knowledge Base contains internal documents such as:

- HR policies
- Leave policies
- IT support documentation
- Employee guidelines
- Company procedures
- Internal knowledge documents

The documents are connected to the Foundry IQ Knowledge Base and searchable through Azure AI Search.

🔗 MCP Integration

Model Context Protocol (MCP) is used to connect the AI Agent with external enterprise tools.

The MCP server is hosted using Azure Functions.

Available MCP Tools
| Tool | Purpose |
|---|---|
| `create_it_ticket` | Creates a new IT support ticket |
| `get_it_ticket` | Retrieves an existing IT ticket |
| `create_leave_request` | Creates an employee leave request |
🎫 IT Ticket Workflow

An employee can simply ask:

Create an IT ticket because my laptop is not connecting to Wi-Fi.

The AI agent understands that an action is required and invokes the MCP tool.

Employee
   │
   ▼
AI Assistant
   │
   ▼
MCP Server
   │
   ▼
create_it_ticket
   │
   ▼
Ticket Created
   │
   ▼
Ticket ID Generated
   │
   ▼
AI Assistant
   │
   ▼
Employee

Example:

Ticket ID : IT-A1B2C3D4
Employee  : Jainish
Issue     : Laptop Wi-Fi not working
Priority  : High
Status    : Open
🛠️ Technology Stack
### Artificial Intelligence
- Microsoft Azure AI Foundry
- Azure AI Agent
- Generative AI
- Retrieval-Augmented Generation (RAG)

### Knowledge & Search
- Foundry IQ Knowledge Base
- Azure AI Search
- Enterprise Documents

### Agent Tools
- Model Context Protocol (MCP)
- Azure Functions
- MCP Tool Triggers

### Backend
- Python
- FastAPI
- Uvicorn

### Frontend
- HTML
- CSS
- JavaScript

### Cloud
- Microsoft Azure
- Azure App Service
- Azure Functions

### Development
- Visual Studio Code
- Git
- GitHub
📁 Project Structure
azure-foundry-enterprise-ai-assistant/
│
├── enterprise-knowledge-agent/
│   │
│   ├── backend/
│   ├── frontend/
│   ├── requirements.txt
│   ├── .env.example
│   └── ...
│
├── mcp-server/
│   │
│   ├── function_app.py
│   ├── requirements.txt
│   ├── host.json
│   └── ...
│
├── knowledge-base/
│   │
│   ├── HR/
│   ├── IT/
│   └── ...
│
├── README.md
└── .gitignore
☁️ Azure Architecture
                         MICROSOFT AZURE
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
          ▼                     ▼                     ▼
   Azure AI Foundry      Azure App Service      Azure Functions
          │                     │                     │
          │                     │                     │
          ▼                     │                     ▼
     Knowledge Base             │               MCP Server
          │                     │                     │
          ▼                     │          ┌──────────┼──────────┐
   Azure AI Search              │          │          │          │
          │                     │          ▼          ▼          ▼
          ▼                     │       Create     Get       Leave
 Enterprise Documents           │       Ticket    Ticket    Request
                                │
                                ▼
                         Web Application
🔐 Security

Sensitive credentials should never be committed to GitHub.

Environment variables and secrets should be configured through Azure App Service / Azure Function App configuration.

Examples:

- `AZURE_ENDPOINT`
- `AZURE_PROJECT_ENDPOINT`
- `AZURE_MODEL`
- `AZURE_SEARCH_ENDPOINT`
- `AZURE_SEARCH_KEY`
- `AZURE_STORAGE_CONNECTION_STRING`

The repository uses .gitignore to prevent sensitive files such as:

- `.env`
- `.env.*`
- `local.settings.json`
- `.venv/`
- `__pycache__/`
- `.DS_Store`

from being committed.

⚙️ Local Setup
Prerequisites

Install the following:

Python 3.x
Visual Studio Code
Git
Azure CLI
Azure Functions Core Tools
1. Clone Repository
git clone https://github.com/Jainish-pixel/azure-foundry-enterprise-ai-assistant.git
cd azure-foundry-enterprise-ai-assistant
▶️ Run Enterprise AI Agent

Navigate to the application:

cd enterprise-knowledge-agent

Create a virtual environment:

python3 -m venv .venv

Activate it:

source .venv/bin/activate

Install dependencies:

pip install -r requirements.txt

Configure the required environment variables.

Run the FastAPI application:

uvicorn main:app --reload

The application will be available at:

http://127.0.0.1:8000
▶️ Run MCP Server

Navigate to the MCP server:

cd mcp-server

Create a virtual environment:

python3 -m venv .venv

Activate:

source .venv/bin/activate

Install dependencies:

pip install -r requirements.txt

Start Azure Functions:

func start

The MCP server will expose the configured MCP endpoints through the Azure Functions host.

☁️ Deployment Architecture

The production deployment is designed around Azure cloud services.

                         GitHub
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
     Enterprise AI Agent            MCP Server
              │                         │
              ▼                         ▼
       Azure App Service         Azure Functions
              │                         │
              └────────────┬────────────┘
                           │
                           ▼
                    Azure AI Foundry
                           │
                  ┌────────┴────────┐
                  │                 │
                  ▼                 ▼
             Knowledge          MCP Tools
               Base
                  │
                  ▼
           Azure AI Search
🔬 Example Queries
Knowledge Retrieval
What is the employee leave policy?
How many annual leave days are available?
What is the IT password reset procedure?
IT Operations
Create an IT ticket for my laptop not connecting to Wi-Fi.
Create a high priority ticket because my VPN is not working.
Find my IT ticket IT-A1B2C3D4.
Leave Operations
Create a leave request for two days.
🎯 Project Objectives

The primary objective of this project is to demonstrate how enterprise organizations can combine:

Generative AI
      +
RAG
      +
Enterprise Knowledge
      +
AI Agents
      +
MCP Tools
      +
Cloud Infrastructure

to create an intelligent assistant capable of both:

1. Knowledge Retrieval

Finding and explaining information from enterprise documents.

2. Enterprise Actions

Executing actions through connected MCP tools.

⭐ Key Benefits
For Employees
Natural language interaction
Faster access to company information
Reduced manual searching
Automated IT ticket creation
Simplified leave requests
For Organizations
Centralized enterprise knowledge
AI-powered document retrieval
Tool-based workflow automation
Scalable cloud architecture
Integration with enterprise systems
🔮 Future Enhancements

Future versions can include:

Microsoft Entra ID authentication
Role-Based Access Control
Microsoft Teams integration
SharePoint integration
Additional MCP tools
Employee profile integration
Approval workflows
Persistent ticket database
Application Insights monitoring
Analytics dashboard
Enterprise-grade authentication and authorization
👥 Team Members
- **JAINISH JINDAL**
- **BHUMIKA**
- **SNEHA**
🏆 Project Title
Enterprise AI Assistant using RAG, MCP & Microsoft Azure
Built with

Microsoft Azure AI Foundry + Foundry IQ + Azure AI Search + RAG + MCP + Azure Functions + FastAPI

🔗 GitHub Repository

Repository:

https://github.com/Jainish-pixel/azure-foundry-enterprise-ai-assistant

📌 Keywords

Azure AI Foundry
Foundry IQ
RAG
Retrieval Augmented Generation
MCP
Model Context Protocol
Azure AI Search
Azure Functions
AI Agent
FastAPI
Generative AI
Enterprise AI
Knowledge Base
Microsoft Azure


**
