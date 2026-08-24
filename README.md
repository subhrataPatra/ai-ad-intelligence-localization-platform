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

```text
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
