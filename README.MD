#  AI-Powered Report Writing Assistant using Gemini + Gradio

A lightweight prototype that leverages Google’s Gemini 1.5 Pro LLM to generate structured reports from raw textual data — designed for market research use cases such as dealer summaries, customer sentiment snapshots, and research digests.

> ⚠️ **Note**: This is an early-stage prototype. Report formats are not finalized — the system is designed to be flexible and easily adapted to your organization's evolving needs.

---

## 📌 Features

- 🔎 Extracts insights from raw research data
- 🤖 Powered by Gemini 1.5 Pro LLM via `google-generativeai`
- 🖥️ Clean Gradio UI — no coding skills needed
- 📤 Exports reports in `.txt`, `.docx`, and `.pdf` formats
- 🌐 Unicode support using `fpdf2` and DejaVuSans font

---

## Use Cases

| Report Type              | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| Dealer Summary           | Summarizes dealer listings by region, services offered, and coverage gaps  |
| Customer Voice Snapshot  | Extracts sentiment, top complaints/praises, and customer suggestions       |
| Research Digest          | Converts raw observations into clean weekly/monthly automotive summaries   |

---

##  Tech Stack

- **LLM**: Google Gemini 1.5 Pro
- **Frontend**: Gradio (Python)
- **Export**: Python-docx, FPDF2 (PDF), DejaVuSans (Unicode)
- **Language**: Python 3.8+

---

##  Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/avulabhumika/gemini-report-assistant.git
cd gemini-report-assistant
````

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

<details>
<summary> <code>requirements.txt</code> sample</summary>

```txt
google-generativeai
gradio
python-docx
fpdf2
```

</details>

### 3. Add Gemini API Key

Create a `.env` file or set the environment variable:

```bash
export GEMINI_API_KEY="your-gemini-api-key"
```

### 4. Download DejaVuSans Font (for PDF export)

[Download Here](https://dejavu-fonts.github.io/Download.html)

Place `DejaVuSans.ttf` in the project root.

---

## ▶️ Running the App

```bash
python report_writer.py
```

Visit `http://localhost:8808` to use the app in your browser.

---

## 📎 Sample Input & Output

**Input:**

```
Dealer: Metro Motors, Mumbai – Offers: Spares & Service
Dealer: Apex Bikes, Pune – Offers: Spares Only
```

**Output Summary:**

* 2 dealers in West Zone
* Both provide spares; 1 also provides service
* Pune may lack sufficient servicing outlets

---

## Flexibility

* Report prompts can be easily customized via `prompt_map` in `report_writer.py`.
* New report types can be added with minimal code changes.

---

##  Project Status

Prototype Completed
Final report structure pending
Ready for internal demo, customization, and integration

---

## License

MIT License. Feel free to fork, contribute, or adapt for your own use cases.

```

