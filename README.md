# AI SKILL: PRACTICAL WORK (KP) REPORT GENERATOR
### Standard Guidelines & Document Generator for University Practical Work Reports (Informatics / Computer Science)

[![Antigravity Skill](https://img.shields.io/badge/Antigravity-Skill-blue.svg)](https://antigravity.google)
[![Recommended Model](https://img.shields.io/badge/AI%20Model-Gemini%204.7--Flash-orange.svg)](https://ai.google.dev)
[![Performance Setting](https://img.shields.io/badge/Thinking%20Budget-Medium%20%7C%20High-green.svg)](#-model--ide-requirements)
[![Document Standard](https://img.shields.io/badge/Document-Word%20.docx%20%7C%20A4%204--3--3--3-purple.svg)](#-mandatory-academic-formatting-standards)

An end-to-end, autonomous **AI Skill module** engineered specifically for the **Google Antigravity IDE** powered by **Gemini 4.7 Flash**. This module guides the AI Agent to master the complete document architecture, chapter layout, academic typography, diagram rendering, and formatting guidelines for University Practical Work (Kerja Praktik / KP) reports, matching 100% with real-world accredited standards:
1. `assets/Laporan_Kerja_Praktik_BKPSDM_Iqsan_Azhar_Nuryadi.pdf` (Original Reference PDF)
2. `assets/dokumen.md` (Project Scope, WBS, and Deliverables)
3. `assets/laporan_kerja_praktik_bkpsdm.md` (Complete Markdown Source Text)
4. `scripts/kp_docx_generator.py` (Automated OpenXML / Python DOCX Rendering Engine)

---

## 🌟 Key Advantages of In-IDE Report Generation

Generating your internship and academic reports directly inside your codebase workspace using **Google Antigravity IDE** delivers massive advantages over traditional manual writing or disconnected web chatbots:

* **🎯 Ground-Truth Precision & Zero Hallucination:**  
  Operating natively within your repository, the AI analyzes your *actual* source code, directory structures, routing files, database migrations, and API implementations. Every architecture diagram, class model, and technical description is grounded in real, functioning code rather than guesswork.
  
* **⚡ Seamless Direct Access to All Project Resources:**  
  The AI agent can instantly inspect commits, test results, configuration files, backend models, and UI components. It automatically aligns the report's Work Breakdown Structure (WBS), Scrum sprints, and feature breakdowns with verified project milestones.

* **🔄 Unified Workflow Without Context Fragmentation:**  
  No more copying and pasting hundreds of lines of code, database schemas, or terminal logs into external browser tabs. Your codebase, diagrams, markdown drafts, and final compiled Microsoft Word (`.docx`) file remain unified in one single version-controlled environment.

* **🚀 End-to-End Autonomous Compilation:**  
  Beyond writing prose, the AI generates valid Mermaid diagrams, converts them to crisp high-DPI PNGs via rendering endpoints, and executes the Python OpenXML engine (`kp_docx_generator.py`) to deliver an accredited, publication-grade document with precise 4-3-3-3 cm margins and multi-section page numbering.

* **⏱️ Instant Real-Time Synchronization:**  
  As your software evolves, refactored APIs or newly added features can be instantly refreshed in the report with a simple chat prompt, guaranteeing that your academic documentation never falls out of sync with your project.

---

## 🤖 Model & IDE Requirements

> [!IMPORTANT]
> **Required AI Model:** **`Gemini 4.7-Flash`**  
> **Recommended Thinking / Reasoning Mode:** **`Medium`** or **`High`** (for maximum context retention, deep architectural analysis, and strict structural adherence).  
>
> All document layouts, chapter breakdown logic, WBS matrices, Mermaid diagram specifications, and table formatting engines in this skill have been thoroughly benchmarked and verified with **Gemini 4.7 Flash**. Using other models may result in inconsistent formatting, missing appendices, or unrendered diagram syntax.

---

## 🚀 Step-by-Step Tutorial: Using in Google Antigravity IDE

Follow these simple steps to install, load, and run this skill in your project:

### Step 1: Open Google Antigravity IDE
Launch your **Google Antigravity IDE** and open your project workspace.

### Step 2: Select the AI Model & Set Performance
1. Open the Antigravity model selection dropdown in the bottom bar or settings panel.
2. Select **`Gemini 4.7-Flash`**.
3. Under the reasoning/thinking budget setting, choose **`Medium`** or **`High`** to enable the AI to deeply inspect project codebases and generate comprehensive academic text without truncating chapters.

### Step 3: Add the Skill to Your Project
Choose one of the following two methods:

* **Method A: Direct Folder in Workspace (Easiest)**
  - Download / extract the ZIP file (or copy the `AI Skill KP generator` folder) directly into your active project root directory.
  
* **Method B: Native Antigravity Skill Discovery**
  - Place this folder into your project's `.agents/skills/` directory:
    ```text
    your-project/
    └── .agents/
        └── skills/
            └── kp-report-generator/
                ├── SKILL.md
                ├── agent.md
                ├── assets/
                ├── scripts/
                └── templates/
    ```
  - Alternatively, place it in your global configuration path at `~/.gemini/config/skills/kp-report-generator/` to make it accessible across all workspaces.

### Step 4: Load and Instruct the AI Agent
Open the Antigravity AI chat panel and prompt the assistant:

> *"Please generate a complete Practical Work (KP) report for student **[Student Name]**, Student ID / NIM **[NIM]**, topic/role: **[Project Title & Role]**, by strictly reading and following the guidelines in `agent.md` (or `@kp-report-generator`)."*

### Step 5: Autonomous Generation & Compilation
Once instructed, the AI Agent will autonomously:
1. **Analyze Your Codebase:** Inspect your project files, commit history, architectural layers, and database schemas.
2. **Draft the Full Academic Report:** Produce the Title Page, Declaration, Approval Sheet, Chapters I through V, References (APA 7th edition), and all 8 Appendices.
3. **Generate & Render System Diagrams:** Write valid Mermaid diagrams (Architecture, Use Case, Class, ERD, Flowchart, Sequence) and render them to crisp PNG images.
4. **Compile to Microsoft Word (`.docx`):** Execute `scripts/kp_docx_generator.py` to output a 100% formatted, print-ready Word document.

---

## 📁 Repository Structure

```text
.
├── SKILL.md                    # Antigravity native skill definition & system prompt
├── agent.md                    # Comprehensive AI Agent rules, instructions & formatting standards
├── README.md                   # Main documentation and quick-start guide
├── assets/
│   ├── logo_unsoed.png         # High-resolution official university crest
│   ├── Laporan_Kerja_Praktik_BKPSDM_Iqsan_Azhar_Nuryadi.pdf # Reference PDF report
│   ├── dokumen.md              # Scope, WBS, and project deliverables reference
│   └── laporan_kerja_praktik_bkpsdm.md # Full reference report markdown source
├── scripts/
│   ├── kp_docx_generator.py    # Python OpenXML rendering engine (Markdown -> Word .docx)
│   └── README.md               # Technical documentation for the Python generator
└── templates/
    └── template_structure.md   # Structural blueprint covering Front Matter, Chapters I-V, & Appendices 1-8
```

---

## 📐 Mandatory Academic Formatting Standards

| Document Component | Enforced Academic Standard |
|---|---|
| **Report Language** | **Formal Academic Indonesian (*Bahasa Indonesia Baku*)** in compliance with university thesis guidelines (EBI). All chapter designations (`BAB I` to `BAB V`), section titles, and narrative text are written in Indonesian, with specialized English technical terms (*framework, backend, API Gateway, middleware*) properly italicized. |
| **Paper & Margins** | **A4** (21.0 × 29.7 cm). Margins: **Left 4.0 cm** (for binding), **Top 3.0 cm**, **Right 3.0 cm**, **Bottom 3.0 cm**. |
| **Typography** | **Times New Roman**, **12 pt** for body paragraphs, **1.5 line spacing**, **1.0 cm first-line indent**, **Justified** alignment. |
| **Page Numbering** | **Cover:** No page number.<br>**Front Matter:** Lowercase Roman numerals (`i, ii, iii...`) at **bottom-right**.<br>**Main Body & Appendices:** Arabic numerals (`1, 2, 3...`) starting at `1` at **bottom-right**. |
| **Table Formatting** | Strips out markdown divider dashes (`---`), headers styled with `#F1F5F9` light gray shading, bold text, `<w:cantSplit/>`, and borderless 2-column signature layout for the approval sheet. |
| **System Diagrams** | High-DPI PNG renderings of Architecture, Use Case, Class, ERD, Flowchart, and Sequence diagrams (no raw markdown or ASCII code in the final DOCX). |
| **Table of Contents** | Formatted using Word-native Tab Stops with Dot Leaders (`.........`) aligned to the 14.0 cm right margin. |
| **Mandatory Appendices** | Full set of **Appendices 1 to 8** (Certificate, Official Agency Acceptance Letter, Grade A Assessment Sheet, 24-Day Attendance Record, Daily Logbook, UAT Matrix, Activity Photos, and Student CV). |

---

## ⚙️ Running the DOCX Generator Manually

If you already have a prepared Markdown draft (`.md`), you can compile it directly into a Microsoft Word (`.docx`) file from the command line:

```bash
# Install the required dependency
pip install python-docx

# Run the generator
python scripts/kp_docx_generator.py \
    --input "path/to/report_draft.md" \
    --output "path/to/KP_Report_Final.docx" \
    --author "STUDENT FULL NAME" \
    --nim "H1D024XXX" \
    --title "FULL TITLE OF PRACTICAL WORK REPORT..."
```

### Command-Line Arguments

| Flag | Short | Required | Description |
|---|:---:|:---:|---|
| `--input` | `-i` | **Yes** | Path to the source Markdown report file (`.md`). |
| `--output` | `-o` | **Yes** | Destination path for the generated Word file (`.docx`). |
| `--author` | `-a` | No | Student full name (auto-detected if omitted). |
| `--nim` | `-n` | No | Student ID number / NIM (auto-detected if omitted). |
| `--title` | `-t` | No | Full report title (auto-detected from first `# Heading 1` if omitted). |
| `--logo` | `-l` | No | Path to official university logo PNG (default: `assets/logo_unsoed.png`). |
| `--diagrams` | `-d` | No | Directory containing pre-rendered diagram PNG images. |

---

## 💡 User Notes & Best Practices

1. **Application Screenshots:**
   - You can instruct the AI to launch your local server and use a browser subagent to capture live UI screenshots.
   - *By default, the AI will not capture automated screenshots* to conserve token context window budget. Instead, it prepares clean figure captions and placeholders so you can insert actual UI screenshots easily, or you can request specific screenshots on demand.
2. **Appendices 1 through 8 as Templates:**
   - The generated appendices (Acceptance Letter, Grade A Evaluation Sheet, 24-Day Attendance, and Logbook) serve as structured reference drafts.
   - For final physical submission, replace them with official scanned documents containing wet ink signatures and institutional stamps.
3. **Mermaid Diagram Rendering:**
   - The generator script automatically queries the Mermaid rendering API to convert diagram code blocks into high-resolution PNG images before inserting them into the Word document.
4. **Table of Contents Page Numbers:**
   - Initial page numbers in the generated Table of Contents, List of Figures, and List of Tables are accurate estimates.
   - You can update all page numbers inside Microsoft Word with a single keypress: press **`Ctrl + A`** then **`F9`** (*Update Entire Table*).
5. **Printer Settings for Physical Binding:**
   - When printing the document for physical hard-cover binding, ensure your printer paper size is strictly set to **A4** (not Letter) to preserve the required 4-3-3-3 cm margin geometry.

---

## 👁️ Previewing DOCX Files Directly in VS Code

To review the generated Microsoft Word file without desktop Microsoft Word (and avoid file locking issues during generation):
1. Install the **DocxViewer** extension in VS Code / Antigravity IDE.
2. Right-click the generated `.docx` file in the Explorer panel.
3. Select **`DOCX Viewer: Open File`**.
4. The document opens immediately in an editor tab without locking the file on disk.

---

## 📄 License & Attribution

This skill was created for students, academic technical writers, and software engineering interns. Maintained by [Iqsan Azhar Nuryadi](https://github.com/iqsanazhr).
