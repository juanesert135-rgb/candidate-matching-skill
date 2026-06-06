# Candidate Matching Agent

## Purpose

The purpose of this agent is to automate the candidate evaluation process and assist recruiters in prioritizing candidates for outreach.

## Inputs

* Job Description A
* Job Description B
* Candidate Resume PDF Files

## Process

### Resume Parsing

The agent extracts:

* Candidate Name
* Years of Experience
* English Level
* Skills
* Education
* Previous Roles

### Candidate Evaluation

The agent evaluates the candidate against both job descriptions and calculates:

* Job A Score
* Job B Score
* Recommendation
* Contact Priority

### Ranking

Candidates are ranked according to their highest score.

## Recommendation Logic

### Job A

Recommended when the candidate demonstrates a significantly stronger fit for Job A.

### Job B

Recommended when the candidate demonstrates a significantly stronger fit for Job B.

### Both

Recommended when both scores are high and closely aligned.

### Neither

Recommended when neither position meets the minimum suitability threshold.

## Outputs

The final output includes:

* Candidate Information
* Scores
* Strengths
* Risks
* Recommendation
* Contact Priority
* Summary

## Human Review

The final hiring decision remains the responsibility of the recruiting team.
