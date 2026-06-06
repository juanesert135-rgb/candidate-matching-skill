# AI Candidate Matching Agent

## Overview

This solution automates candidate screening and ranking for multiple job openings using AI and workflow automation.

The system processes candidate resumes, extracts structured information, evaluates candidates against multiple job descriptions, assigns scores, generates recommendations, and publishes results to Notion.

## Features

* Resume parsing using AI
* Candidate scoring against multiple job descriptions
* English proficiency extraction
* Skills extraction
* Strengths and risk identification
* Candidate prioritization
* Automated reporting in Notion

## Workflow Architecture

1. Load Job Descriptions
2. Load Candidate Resumes
3. Extract Resume Text
4. AI Resume Parsing
5. Candidate Evaluation
6. Ranking and Prioritization
7. Store Results in Notion

## Output

For each candidate:

* Candidate Name
* Years of Experience
* English Level
* Skills
* Job A Score
* Job B Score
* Recommendation
* Contact Priority
* Strengths
* Risks
* Summary

## Technologies Used

* n8n
* OpenAI
* Notion API

## Reproducibility

The workflow can be reused for future job descriptions by simply replacing the job description files without modifying the workflow logic.
