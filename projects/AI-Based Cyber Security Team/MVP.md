## Agentic Pen tester the execute SQL injection
- Use UI like LibreChat or Open-webUI for chatting with the agent
- Agent must be able to run sandbox environments (needs research)
	- can be a tool that starts docker container with kalilinux image
	- to execute commands in there, it can use docker exec ...
		- other way is to prepare scripts to execute in custom docker image instead of generating commands everytime
- Prepare simple SQL-Injection scenario and write the required prompt
- NOTE: This sounds like a solution that doesnt need Agents or Generative AI