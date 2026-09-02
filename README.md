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
Choose one of the following two setup options:

* **Option A: Native Antigravity Skill Location (Recommended)**  
  Place the extracted skill folder into your project's `.agents/skills/` directory as `kp-report-generator`:
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
  *(Or place it globally in `~/.gemini/config/skills/kp-report-generator/` on Linux/macOS or `%USERPROFILE%\.gemini\config\skills\kp-report-generator\` on Windows to make it automatically available across all projects).*

* **Option B: Direct Workspace Folder**  
  Simply extract the ZIP or copy the `AI Skill KP generator` folder directly into your project's root folder.

---

### Step 4: How to Load the Skill in Antigravity

Antigravity gives you multiple easy ways to load and activate the skill:

1. **Direct Mention via `@` Tag:**  
   In the Antigravity chat input box, type `@kp-report-generator` to instantly attach and activate the skill context.
   
2. **Explicit Chat Command:**  
   Type in chat:
   > *"Load skill `kp-report-generator` (or read `agent.md`) and create my Practical Work report."*
   
3. **Automatic On-Demand Discovery:**  
   Because the folder contains `SKILL.md` with standard frontmatter metadata, Antigravity automatically indexes the skill and activates it whenever you ask questions or give instructions related to practical work (KP) reports, thesis documentation, or university internship reports.

---

### Step 5: Interactive Intake Confirmation (Name, NIM, Title, & Screenshot Choice)

Once loaded, the AI Agent will proactively ask and confirm 4 critical project inputs with you before writing:
1. **Student Full Name (*Nama Lengkap Mahasiswa*)**
2. **Student ID / NIM (*Nomor Induk Mahasiswa*)**
3. **Full Report Title (*Judul Laporan Kerja Praktik*)**
4. **Screenshot Option (*Opsi Pengambilan Screenshot*):**  
   The AI will prompt you to choose how application screenshots should be handled:
   * **Option A (Default & Highly Recommended): Formatted Placeholders & Captions**  
     The AI creates clean, standardized figure captions and placeholders so you can paste genuine UI screenshots manually. *This conserves maximum context window tokens and guarantees lightning-fast generation.*
   * **Option B (⚠️ NOT RECOMMENDED): Automated Browser Subagent Screenshots**  
     The AI starts local servers and commands a browser subagent to take live screenshots of the UI.  
     *⚠️ Advisory Warning:* Automated screenshot capturing consumes an immense amount of conversational context window tokens, which can cause token budget exhaustion and slower responses.

---

### Step 6: Autonomous Generation & Compilation

After confirming your intake details, the AI Agent will autonomously:
1. **Analyze Your Codebase:** Inspect directory structures, database migrations, controllers, models, and Git commit histories.
2. **Draft the Full Academic Report in Indonesian:** Author the complete front matter, Chapters I to V, APA 7th References, and all 8 accredited Appendices in formal academic Indonesian (*Bahasa Indonesia Baku*).
3. **Render System Diagrams:** Formulate 6 software engineering models (Architecture, Use Case, Class, ERD, Flowchart, Sequence) in Mermaid syntax and automatically render them to high-DPI PNGs.
4. **Compile to Microsoft Word (`.docx`):** Run `scripts/kp_docx_generator.py` to produce a 100% formatted, print-ready Word document with standard A4 4-3-3-3 cm margins and multi-section page numbering.

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
│   ├── capture_screenshots.py  # Automated Playwright & Chrome screenshot capture engine
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

## 📸 Automated Web & Mobile Screenshot Engine

You can automatically take screenshots of all active web portals (admin, kiosk, consultations, public surveys) and mobile screens using the included Playwright automation script:

```bash
# Install dependencies
pip install playwright
playwright install chromium

# Run the automated screenshot capture
python scripts/capture_screenshots.py \
    --output-dir "extracted_assets/screenshots" \
    --base-url "http://127.0.0.1:8000" \
    --kios-url "http://127.0.0.1:8003" \
    --konsul-url "http://127.0.0.1:8002" \
    --survei-url "http://127.0.0.1:8001" \
    --username "admin" \
    --password "password123" \
    --periode-mulai "2026-08-01" \
    --periode-selesai "2026-08-31"
```

### 🧠 Project-Adaptive Reconnaissance Capability:
The AI Agent doesn't just run a static script; it possesses an **Autonomous Workspace Reconnaissance Protocol**:
* **Tech-Stack & Route Inspection:** Analyzes routes, auth controllers, and `.env` files to locate genuine login credentials (e.g. usernames, NIPs, or emails).
* **Multi-Role Login Automation:** Dispatches requests through authenticated sessions (Super Admin, Staf, or End-User) based on the target page.
* **Full-Page Long Scrolling (`full_page=True`):** Captures complete vertical layouts for long submission forms (Online Consultations, Kiosks, 9-question Likert scale IKM surveys) without clipping submit buttons.
* **In-Session Seeding & Date Alignment:** Overcomes the "blank state" trap on daily dashboards and calendars by seeding 3–5 authentic records for today and configuring calendar focus to the active internship month (e.g. August 2026).
* **Flutter Headless Web Emulation:** Compiles Flutter mobile apps to web (`flutter build web --release`) and hosts them locally (e.g. port 5000), using flagship Android viewports (`412x860`, `device_scale_factor: 2.0`) to capture real mobile Bento Grids, chat rooms, and workspaces without heavy Android Studio emulators.
* **Dynamic Parameter Injections:** Generates active HMAC session tokens to prevent expired states, and applies date filters matching the user's specific internship period.
* **Unified 30-Figure Standard:** Fully manages and embeds 30 publication-grade diagrams and system screenshots into the report.
* **Custom Script Synthesis:** The AI automatically writes or updates `scripts/capture_screenshots.py` specifically tailored to whatever project repository it is loaded into!

---

## 🖨️ Automated Native PDF Export via Word COM (Windows)

On Windows machines with Microsoft Word installed, you can produce a 100% exact, publication-ready PDF with high-DPI images, accurate Table of Contents pagination, and zero layout drift using the native Word COM automation pipeline:

```python
import os, win32com.client, shutil

doc_path = os.path.abspath("path/to/Laporan_KP.docx")
pdf_path = os.path.abspath("path/to/Laporan_KP.pdf")

word = win32com.client.Dispatch("Word.Application")
word.Visible = False
try:
    doc = word.Documents.Open(doc_path)
    doc.SaveAs(pdf_path, FileFormat=17) # 17 = wdFormatPDF
    doc.Close()
    print(f"SUCCESS: Exported PDF ({os.path.getsize(pdf_path)} bytes)")
finally:
    word.Quit()
```

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
