# MATACS Technical Assessment

Candidate: Aqsa Nazir
Position: Associate Software Developer  
Assessment Reference: MATACS-TH-2026-02  
Time Spent: 2 hours

## Project Overview

This repository contains a system design for an AI-assisted contractor proposal evaluation tool.

The proposed system allows administrators to configure evaluation criteria, reviewers to upload contractor proposals, and AI to extract relevant information from proposal documents. A deterministic rule-based scoring engine checks mandatory requirements, calculates weighted scores, and generates explainable rankings. Human reviewers retain responsibility for the final award decision.

## Design Principles

- Use AI for document understanding and information extraction, not for independently determining final rankings.
- Use configurable, deterministic rules for mandatory checks, eligibility, and scoring.
- Provide transparent explanations and supporting evidence for each score.
- Flag missing, ambiguous, or uncertain information for human review.
- Maintain an audit trail of evaluation results and criteria changes.
- Treat uploaded proposal content as untrusted data.

## Repository Contents

- [Process Flow Diagram](diagram/process_daigram.jpg)
- [Design Write-up](WRITEUP.md)
- [AI Prompts](PROMPTS.md)
- [Expected Rankings](ranking.json)

## AI Tool Usage

I used ChatGPT to understand existing platforms such as Upwork and Fiverr and explore how their ranking mechanisms could inform this proposal evaluation system. 
I also used it to clarify the assessment requirements, explore document extraction, weighted scoring, and tie-breaking approaches, and compare possible design solutions. 
I refined the proposed approach to ensure that mandatory checks, score calculations, and ranking decisions follow explicit, configurable rules, with human reviewers making the final award decision.