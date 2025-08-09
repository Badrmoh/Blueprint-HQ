# Properties
- Agentic AI based Pen Tester
- Ability to create sandboxes for carrying out tasks
- Generate Reports
- User

# Data Properties
- Data Collected deleted as soon as Reports generated?
	- Do we need to store data? yes for interactively ask about it or to explain it.
- What kind of data should be used?
	- Tests Instructions
	- Report Generation instructions
	- Sandbox instructions
	- historical data?

# Workflow
- User asks to run certain tests, or full test, and gives the url
- Agents kick off and start preparing environments accordingly.
- Agents start collecting information according to the test case scenario
- Agents start to run tests in sandbox environment
- Actively collect output like error messages to know more about the target system and how to exploit it in context of the test case.
- Agent conclude tests and generate a report
- An interactive chatbot comes up for chatting with the report.

# External Integrations
- Maybe Jira or confluence, to push test results or reports.