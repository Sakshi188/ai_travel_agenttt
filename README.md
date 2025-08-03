Welcome to the AI Travel Agent repository! This project demonstrates how to leverage LangGraph for building a smart travel assistant that uses multiple language models (LLMs) to handle tasks such as finding flights, booking hotels, and sending personalized emails. The agent is designed to interact with users, invoke necessary tools, and provide a seamless travel planning experience.

Features
Stateful Interactions: The agent remembers user interactions and continues from where it left off, ensuring a smooth user experience.
Human-in-the-Loop: Users have control over critical actions, like reviewing travel plans before emails are sent.
Dynamic LLM Usage: The agent intelligently switches between different LLMs for various tasks, like tool invocation and email generation.
Email Automation: Automatically generates and sends detailed travel plans to users via email.
Getting Started
Clone the repository, set up the virtual environment, and install the required packages

git clone git@github.com:nirbar1985/ai-travel-agent.git

( In case you have python version 3.11.9 installed in pyenv)

pyenv local 3.11.9
Install dependencies

poetry install --sync
Enter virtual env by:

poetry shell
Store Your API Keys
Create a .env file in the root directory of the project.
Add your API keys and environment variables to the .env file:
OPENAI_API_KEY=your_openai_api_key
SERPAPI_API_KEY=your_serpapi_api_key
SENDGRID_API_KEY=your_sendgrid_api_key

# Observability variables
LANGCHAIN_API_KEY=your_langchain_api_key
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=ai_travel_agent
Make sure to replace the placeholders (your_openai_api_key, your_serpapi_api_key, your_langchain_api_key, your_sendgrid_api_key) with your actual keys. This version includes the necessary environment variables for OpenAI, SERPAPI, LangChain, and SendGrid and the LANGCHAIN_TRACING_V2 and LANGCHAIN_PROJECT configurations.

How to Run the Chatbot
To start the chatbot, run the following command:
  streamlit run app.py
Using the Chatbot
Once launched, simply enter your travel request.


Email Integration
The email integration is implemented using the human-in-the-loop feature, allowing you to stop the agent execution and return control back to the user, providing flexibility in managing the travel data before sending it via email.
For example:

I want to travel to Amsterdam from Madrid from October 1st to 7th. Find me flights and 4-star hotels.
