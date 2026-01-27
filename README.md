# Technical-writer-agent-a2a
This is about creating simple remote agents that interact with one another by using Microsoft Foundry thru A2A protocol. These agents will assist technical writers with preparing their developer blog posts. A title agent will generate a headline, and an outline agent will use the title to develop a concise outline for the article.
## Steps:
### Step 1:
Create a Foundry project at ai.azure.com with gpt-4o deployment, noting the endpoint.
### Step 2:
Clone the GitHub repo (mslearn-ai-agents), set up a Python venv, install dependencies (azure-ai-projects, azure-ai-agents, a2a-sdk), and configure .env with project endpoint.
### Step 3:
Implement the title agent in agent.py (using AgentsClient, create_agent) and server.py (AgentCard, skills, A2AStarletteApplication).
Same concept applies to the outline agent as well, the agent.py would be deployed with the server.py.


### Agent interactions:
The routing agent discovers remote agents via A2A, sends async messages (SendMessageRequest), and orchestrates responses.
Title agent's agent_executor.py handles execute/cancel with task updates and agent.run_conversation.

### Running:
Run az login then python "run_all.py" to launch servers and test (e.g., "Create a title for Microsoft Foundry by using A2A article")
