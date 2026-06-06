# Notion MCP Setup Instructions

## Purpose

This workflow stores candidate evaluation results in a Notion database. To execute the skill with new job descriptions and candidates, the Notion integration must be connected to the evaluator's environment.

---

## Prerequisites

* Notion account
* Notion workspace
* Access to the repository
* OpenAI API Key
* n8n instance

---

## Step 1: Create a Notion Integration

1. Open Notion.
2. Navigate to Settings → Connections → Develop or manage integrations.
3. Create a new integration.
4. Name the integration.
5. Copy the Internal Integration Token.

---

## Step 2: Create the Candidate Database

Create a Notion database named:

Candidate Ranking

Recommended properties:

| Property         | Type      |
| ---------------- | --------- |
| Candidate        | Title     |
| Job A Score      | Number    |
| Job B Score      | Number    |
| English Level    | Select    |
| Recommendation   | Select    |
| Contact Priority | Select    |
| Skills           | Rich Text |
| Strengths        | Rich Text |
| Risks            | Rich Text |
| Summary          | Rich Text |

---

## Step 3: Share the Database with the Integration

1. Open the Candidate Ranking database.
2. Click Share.
3. Open Connections.
4. Connect the integration created in Step 1.
5. Confirm edit permissions.

---

## Step 4: Configure n8n Credentials

Create a Notion API credential in n8n.

Credential Type:

Notion API

Required Value:

NOTION_API_TOKEN=<your_notion_token>

---

## Step 5: Import Workflow

Import:

workflow/candidate_matching_workflow.json

into n8n.

---

## Step 6: Configure OpenAI Credentials

Create an OpenAI credential in n8n.

Required:

OPENAI_API_KEY=<your_openai_key>

---

## Step 7: Update Job Descriptions

Replace the Job A and Job B input documents with the new vacancy descriptions.

No workflow modifications are required.

---

## Step 8: Execute

Run the workflow.

The system will:

1. Process candidate resumes.
2. Extract structured candidate information.
3. Evaluate candidates against both job descriptions.
4. Generate scores and recommendations.
5. Rank candidates.
6. Store the results in the Notion database.

---

## Repository Structure

candidate-matching-agent/

* README.md
* agent.md
* workflow/candidate_matching_workflow.json
* prompts/resume_parser.txt
* prompts/candidate_evaluator.txt
* docs/notion_mcp_setup.md

---

## Notes

The workflow was designed to be reusable for future hiring processes. New job descriptions can be evaluated without modifying the workflow logic.
