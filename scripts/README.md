# USAGE GUIDE: `kp_docx_generator.py`
### Automated Practical Work (KP) Report Generator (Markdown -> Word .docx)

The `kp_docx_generator.py` script is a standalone Microsoft Word (`.docx`) document generator engineered specifically to meet the academic thesis and Practical Work (Kerja Praktik / KP) formatting guidelines of the Department of Informatics, Faculty of Engineering, Universitas Jenderal Soedirman.

---

## ⚙️ System Requirements & Dependencies

* **AI Developer Model:** **Gemini 4.7 Flash** *(All markdown report drafting, table structuring, and chapter logic were benchmarked using this model)*.
* **Environment:** Python 3.8+
* **Python Packages:** `python-docx`

```bash
pip install python-docx
```

---

## 🚀 How to Run the Script

The script can be executed directly from your terminal or command prompt:

### Basic Syntax:
```bash
python kp_docx_generator.py --input <markdown_file_path> --output <docx_file_path> [optional_flags]
```

### Complete Example Command:
```bash
python "scripts/kp_docx_generator.py" \
    --input "assets/laporan_kerja_praktik_bkpsdm.md" \
    --output "Laporan_KP_Final.docx" \
    --author "IQSAN AZHAR NURYADI" \
    --nim "H1D024009" \
    --title "RANCANG BANGUN SISTEM BACKEND, RESTFUL API GATEWAY, DAN INTEGRASI MULTI-SERVICE PELAYANAN..."
```

---

## 📋 Command-Line Arguments (CLI)

| Parameter | Short | Required? | Description & Default Value |
|---|:---:|:---:|---|
| `--input` | `-i` | **Yes** | Path to the source Markdown report file (`.md`). |
| `--output` | `-o` | **Yes** | Destination path for the generated Word document (`.docx`). |
| `--author` | `-a` | No | Student author full name (auto-detected from markdown if omitted). |
| `--nim` | `-n` | No | Student ID number / NIM (auto-detected from markdown if omitted). |
| `--title` | `-t` | No | Full report title (auto-detected from first `# Heading 1` if omitted). |
| `--logo` | `-l` | No | Path to official university logo PNG (default: `../assets/logo_unsoed.png`). |
| `--diagrams`| `-d` | No | Directory containing pre-rendered diagram PNG images. |

---

## ✨ Core Features & Enforced Formatting Standards

1. **Paper Format & 4-3-3-3 cm Margins:**
   * Paper Size: A4 (21.0 × 29.7 cm).
   * Left Margin: **4.0 cm** (binding allowance).
   * Top, Right, Bottom Margins: **3.0 cm** each.
2. **Academic Typography & Paragraph Spacing:**
   * Standard Font: *Times New Roman*, 12 pt, 1.5 line spacing, *Space After* 6 pt.
   * Text Alignment: *Justified*.
   * First-Line Indent: **1.0 cm**.
3. **Automated Multi-Section Page Numbering:**
   * **Cover Page:** Clean and unnumbered.
   * **Front Matter (*Declaration to List of Tables*):** Lowercase Roman numerals (**`i, ii, iii...`**) in the bottom-right footer.
   * **Main Body (*BAB I to Appendix 8*):** Arabic numerals (**`1, 2, 3...`**) starting at `1` in the bottom-right footer.
4. **Automated Table Cleanup:**
   * Detects and removes markdown table divider rows (such as `|:---:|---|---|`), ensuring no raw dashes appear in the generated Word document.
   * Applies professional soft gray header shading (`#F1F5F9`), bold text, and `<w:tblHeader/>` to repeat headers across page breaks.
   * Appends `<w:cantSplit/>` to prevent rows from breaking awkwardly across pages.
   * Renders approval sheet signature tables borderless.
5. **Table of Contents with Dot Leaders:**
   * Applies native Word tab stops with dot leaders (`.........`) aligned to the 14.0 cm right margin.
6. **File Locking Fallback (*Permission Handling*):**
   * If the target `.docx` file is currently open in Microsoft Word, the script will not crash; it automatically writes to an alternate path (e.g., `_New.docx`).

---

## 👁️ Previewing Documents in VS Code

To view generated Word documents directly inside VS Code without desktop Microsoft Word:
1. Open the `.docx` file in VS Code Explorer.
2. Right-click and choose **`DOCX Viewer: Open File`**.
3. The document is displayed in an editor tab without locking the file on disk.
