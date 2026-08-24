# AI Ad Intelligence & Localization Platform

A production-oriented AI automation platform for researching advertising,
analyzing creatives and messaging, localizing campaigns for different
markets, and supporting AI-assisted creative generation.

## Overview

This project automates a multi-stage advertising intelligence and
localization workflow using n8n, LLMs, external APIs, structured data,
and human review.

It is a long-term project involving **300+ hours of hands-on design,
implementation, testing, and workflow refinement**.

The platform brings together ad research, AI analysis, localization,
creative generation, and human review into a connected workflow rather
than treating each activity as a separate process.

## What It Does

The platform supports multiple stages of the advertising intelligence and
localization process:

- 🔎 Competitor ad research and data collection
- 🧹 Ad filtering and data normalization
- 🧠 AI-based classification and marketing attribute extraction
- 📊 Creative and messaging analysis
- 🌍 Localization analysis and translation
- 🎨 AI-assisted creative generation
- 👤 Human-in-the-loop review
- 🔄 Rerun and post-review processing
- 📦 Structured outputs for downstream workflows

## High-Level Workflow

Ad Research
     ↓
Data Collection
     ↓
Filtering & Normalization
     ↓
AI Analysis
     ↓
Classification & Attribute Extraction
     ↓
Localization & Translation
     ↓
Creative Generation
     ↓
Human Review
     ↓
Approved → Final Output
     │
     └── Changes Required
                ↓
          Rerun / Reprocess

## Technology Stack

| Area | Technology |
|---|---|
| Workflow Automation | n8n |
| LLM Processing | OpenAI / LLM APIs |
| Data Collection | Apify |
| Data Management | Airtable |
| Creative Generation | Replicate |
| Integrations | REST APIs / Webhooks |
| Data Format | JSON |


## Key Engineering Focus

### Structured AI Processing

LLM outputs are handled as structured data with defined fields and
validation before being passed to downstream workflow steps.

### Modular Workflow Design

The platform is divided into logical workflow stages and reusable
sub-workflows, making individual components easier to test and modify.

### Human-in-the-Loop

Human review is included at points where creative or business judgment
is important. Reviewed items can continue through the workflow or be
sent back for reprocessing.

### Rerunnable Workflows

The workflow supports targeted reruns after human feedback instead of
requiring the entire pipeline to be executed again.

### Reliability

Inputs, API responses, and intermediate outputs are validated to prevent
incorrect or incomplete data from silently moving through the workflow.

## My Contribution

I designed and implemented the core automation architecture, including:

- n8n workflow design and development
- API and webhook integrations
- Apify data collection
- Airtable data structures
- LLM prompt and processing design
- Structured output handling
- Validation and error handling
- Localization and translation workflows
- AI-assisted creative generation
- Human-in-the-loop workflows
- Rerun and post-review processing
- Testing and workflow refinement

## Repository Structure

```text
architecture/    → System architecture and workflow diagrams
docs/            → Technical documentation
examples/        → Sanitized sample inputs and outputs
workflows/       → Sanitized workflow examples
prompts/         → Prompt design and AI processing notes
