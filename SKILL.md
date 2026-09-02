---
name: kp-report-generator
description: Autonomous Academic AI Skill for Google Antigravity (Gemini 4.7-Flash) to generate standardized, publication-grade University Practical Work (Kerja Praktik) reports in Markdown and Microsoft Word (.docx).
---

# Antigravity Skill: Practical Work (KP) Report Generator

This skill teaches the Antigravity AI Agent (powered by **Gemini 4.7 Flash**) how to autonomously author, structure, format, and compile comprehensive University Practical Work (Kerja Praktik / KP) reports following accredited Computer Science / Informatics university guidelines.

## Requirements
- **AI Model:** `Gemini 4.7-Flash`
- **Reasoning Mode:** `Medium` or `High` (in Antigravity model settings)
- **Environment:** Python 3.8+ with `python-docx` installed

## Quick Start & Usage

### 1. Mandatory User Intake Protocol
Before drafting or compiling the report, the AI Agent **must proactively ask and confirm** with the user:
1. **Student Full Name (*Nama Lengkap*)**
2. **Student NIM (*Nomor Induk Mahasiswa*)**
3. **Report Title (*Judul Laporan Kerja Praktik*)**
4. **Screenshot Option (*Opsi Screenshot*):** Give the user the choice between:
   - *(Recommended)* AI creates formatted captions & placeholders for manual insertion (saves token context budget).
   - *(⚠️ Not Recommended)* AI captures automated browser screenshots (advising the user that this consumes a very high token budget).

### 2. Autonomous Execution
Once confirmed, the AI Agent will:
1. Inspect your workspace codebase and project deliverables.
2. Draft the complete academic report covering the Cover, Declaration, Approval Sheet, Chapters I to V, APA 7th References, and all 8 Appendices.
3. Formulate and render 6 software engineering diagrams (Architecture, Use Case, Class, ERD, Flowchart, Sequence) via Mermaid API to PNG.
4. Run `python scripts/kp_docx_generator.py` to compile the final `.docx` report with 4-3-3-3 cm margins, proper page numbering, and clean tables.

> **Note on Report Language:** While instructions and skill definitions are in English, the generated report itself (all chapters BAB I to V, tables, captions, and appendices) **MUST be written in formal academic Indonesian (*Bahasa Indonesia Baku*)** conforming to Indonesian university thesis standards.

For full rules and detailed structural breakdowns, refer to [`agent.md`](file:///d:/lokal%20bkpsdm/AI%20Skill%20KP%20generator/agent.md) and [`README.md`](file:///d:/lokal%20bkpsdm/AI%20Skill%20KP%20generator/README.md).
