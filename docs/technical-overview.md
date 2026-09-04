# Technical Overview

## System Purpose

The AI Ad Intelligence & Localization Platform is a multi-stage automation system designed to streamline advertising research, creative analysis, localization, and AI-assisted content generation.

The system connects data collection, AI processing, workflow orchestration, human review, and operational monitoring into a single workflow.

## Workflow Architecture

The system is organized into modular workflow stages:

1. **Ad Research & Data Collection**
   - Collects advertising data using Apify and external APIs.
   - Supports competitor and product research.

2. **Filtering & Normalization**
   - Filters collected data based on workflow requirements.
   - Normalizes information before downstream processing.

3. **AI Analysis**
   - Uses LLMs for classification, marketing attribute extraction, creative analysis, and messaging analysis.
   - Produces structured outputs for downstream workflow steps.

4. **Localization**
   - Performs localization analysis and translation for different markets.
   - Supports market-specific creative preparation.

5. **Creative Generation**
   - Uses AI-assisted creative generation to produce localized creative outputs.

6. **Human Review**
   - Human review is introduced where creative or business judgment is required.
   - Reviewers can approve outputs or provide feedback for further processing.

7. **Rerun & Reprocessing**
   - Reviewer feedback can trigger targeted reruns.
   - The workflow can reprocess the relevant stage instead of executing the entire pipeline again.

## Data & Integration Layer

The platform uses:

- **n8n** for workflow orchestration
- **Airtable** for structured data management and workflow state
- **Apify** for data collection
- **OpenAI / LLM APIs** for AI processing
- **Replicate** for AI-assisted creative generation
- **REST APIs and webhooks** for external integrations
- **JSON** for structured data exchange

## Reliability & Validation

The workflow is designed to avoid silently passing incorrect or incomplete data between stages.

Key reliability mechanisms include:

- Input validation
- API response validation
- Structured LLM outputs
- Intermediate data validation
- Error handling
- Human review for uncertain outputs
- Targeted reruns after review feedback
- Workflow status tracking and monitoring

## Design Principles

The system follows several core design principles:

- **Modularity** — individual workflow stages can be developed and tested independently.
- **Structured processing** — AI outputs are handled as structured data rather than unvalidated free-form text.
- **Human-in-the-loop** — human judgment is retained where automation alone is not sufficient.
- **Recoverability** — failed or unsatisfactory outputs can be reprocessed without restarting the entire pipeline.
- **Production orientation** — validation, error handling, testing, and monitoring are treated as part of the system design.
