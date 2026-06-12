# AI-Powered Editorial Review Workflow

## Overview

The AI-Powered Editorial Review Workflow automates manuscript quality review by combining workflow orchestration, document processing, and local large language models (LLMs).

The solution retrieves a manuscript, character bible, outline, and style guide, then performs chapter-by-chapter analysis to identify continuity issues, editorial concerns, missing story beats, and AI-generated prose patterns.

The workflow was built using n8n and Ollama with the Qwen 14B model, enabling fully local processing of unpublished manuscripts without sending content to third-party AI services.

---

## Business Problem

Developmental editing requires authors and editors to repeatedly compare manuscript chapters against multiple reference documents.

This process is:

* Time consuming
* Difficult to perform consistently
* Repetitive across multiple review passes
* Prone to missed continuity errors

A full manuscript review can require many hours of manual comparison between:

* Manuscript draft
* Character bible
* Story outline
* Style guide

---

## Solution

This workflow automates the editorial review process by:

1. Retrieving manuscript reference materials from Google Docs.
2. Merging all contextual information into a single analysis package.
3. Parsing the manuscript into individual chapters.
4. Sending each chapter through a local LLM for analysis.
5. Generating structured editorial feedback.
6. Consolidating findings into a centralized editorial report.

---

## Technologies Used

### Workflow Orchestration

* n8n

### Artificial Intelligence

* Ollama
* Qwen3 14B

### Data Sources

* Google Docs

### Processing

* JavaScript
* Prompt Engineering
* Document Parsing

---

## Workflow Architecture

See Architecture Diagram

---

## Workflow Steps

### 1. Retrieve Reference Materials

The workflow retrieves:

* Character Bible
* Story Outline
* Style Guide
* Novel Manuscript

### 2. Merge Context

All documents are consolidated into a single context package for analysis.

### 3. Parse Chapters

The manuscript is automatically split into chapters using chapter pattern detection.

### 4. Analyze Chapters

Each chapter is evaluated against:

* Character continuity
* Story outline compliance
* Style guide adherence
* Narrative structure
* AI-writing indicators

### 5. Generate Editorial Notes

Structured findings are produced for:

* Continuity Issues
* Editorial Notes
* AI Prose Flags
* Missing Outline Beats
* Strengths

### 6. Consolidate Results

All chapter analyses are appended to a master editorial report.

---

## Estimated Impact

Before Automation:

* 45–60 minutes manual review per chapter

After Automation:

* 2–5 minutes automated analysis per chapter

Estimated Reduction:

* 90–95% reduction in manual review effort

---

## Lessons Learned

* AI output quality depends heavily on contextual information.
* Structured prompts produce significantly more consistent results.
* Local LLM deployment protects sensitive manuscript content.
* Workflow orchestration is often more important than model selection.
* Breaking large documents into smaller processing units improves output quality and reliability.

---

## Future Enhancements

* Automated severity scoring
* Character relationship tracking
* Plot thread tracking
* Multi-model review comparison
* Editor approval workflow
* PDF export generation
