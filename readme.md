E1 – Environment Setup & Developer Readiness
🎯 Objective
Prepare developers to create, test, and deploy basic GenAI scripts and prototypes using the correct environment, tools, and API fundamentals.
⚙️ Prerequisites
Basic knowledge of Python and REST APIs
Azure AD / Enterprise account access
AVD (Azure Virtual Desktop) or local Windows machine
Internet access to reach Azure OpenAI endpoints
🧰 What to Learn
🔹 1. Environment Setup (Infrastructure Readiness)
How to request, configure, and log in to your Azure Virtual Desktop (AVD)
Installing essential development tools:
Python 3.10+
Visual Studio Code
Git (for version control)
Postman (for API testing)
Azure CLI (for resource access)
Setting up your Python virtual environment:
python -m venv genai-env
source genai-env/bin/activate   # Mac/Linux
genai-env\Scripts\activate      # Windows
Installing required libraries:
pip install openai langchain streamlit requests python-dotenv
🔹 2. API Fundamentals
Understanding RESTful APIs (methods, headers, payloads, auth)
API authentication (API Key vs. Azure AD token)
Calling OpenAI API endpoints from Python:
from openai import OpenAI
client = OpenAI(api_key="YOUR_API_KEY")
response = client.chat.completions.create(
    model="gpt-4",
    messages=[{"role": "user", "content": "Explain Generative AI"}]
)
print(response.choices[0].message.content)
Using Azure OpenAI endpoint structure:
https://<your-resource-name>.openai.azure.com/openai/deployments/<deployment-name>/chat/completions?api-version=2024-03-01-preview
🔹 3. Development Workflow (Code + Environment Hygiene)
Folder structure for GenAI projects:
genai-project/
├── .env
├── main.py
├── utils/
├── data/
└── requirements.txt
Managing API keys securely with .env files and python-dotenv
Logging and debugging tips (using logging module)
Using Git for version control and collaboration
🔹 4. Hands-On Developer Labs
Lab	Description	Skills Covered
Lab 1: Hello GenAI	Run a simple LLM query using OpenAI or Azure OpenAI	API call basics
Lab 2: Summarizer	Summarize a paragraph or email	Prompt creation
Lab 3: Chat Interface	Build a Streamlit chatbot	UI + API integration
Lab 4: Data Extractor	Extract insights from text or JSON	Parsing + LangChain basics
🔹 5. Troubleshooting & Best Practices
Common API errors and how to debug:
401 Unauthorized → check API key
429 Too Many Requests → rate limit handling
400 Bad Request → invalid model or parameter
Performance optimization: prompt brevity, caching responses
Cost monitoring and token usage awareness
🧠 Outcome
By the end of E1, a developer will:
✅ Have a fully configured AVD or local GenAI environment
✅ Understand how to call and manage LLM APIs programmatically
✅ Be able to create, test, and debug GenAI scripts
✅ Follow good development hygiene (version control, environment isolation, API security)
📦 Tools & Tech Stack Summary
Category	Tool	Purpose
IDE	Visual Studio Code	Development
Language	Python 3.10+	Core programming
Libraries	openai, langchain, streamlit, dotenv, requests	Core SDKs
API Tools	Postman, Azure CLI	Testing and setup
Platform	Azure Virtual Desktop	Managed workspace
Repo	GitHub / Azure DevOps	Code management
Would you like me to integrate this E1 Developer-Ready version into your full E0–E5 framework document and generate a formatted PDF training manual (with headers, visuals, and learning tables)?
It’ll look like a corporate-ready enablement guide you can distribute to participants or publish internally.
