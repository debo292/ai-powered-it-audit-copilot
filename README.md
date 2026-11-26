# IT Audit Copilot

A portfolio MVP demonstrating how generative AI can assist IT auditors with evidence triage, control mapping, preliminary gap identification and audit documentation.

## What it does
- Dashboard with fictional control assessment examples
- Seven-control starter library across IAM, change, vulnerability, patching, backup and monitoring
- Evidence upload for CSV, TXT, MD and text-based PDF
- LLM-assisted preliminary assessment when an OpenAI API key is configured
- Deterministic demo mode when no API key is configured
- JSON assessment export

## Important
This is an experimental portfolio prototype, not an audit tool approved for production. Use synthetic data only. Never upload employer, client, bank, customer, employee or otherwise confidential information. AI outputs can be wrong and must be checked against original evidence by a qualified auditor. A language model cannot establish evidence authenticity, completeness or operating effectiveness by itself.

## Setup (Windows / macOS / Linux)
1. Install Python 3.10 or newer.
2. Extract this project and open a terminal in the project folder.
3. Create and activate a virtual environment:

   Windows:
   `python -m venv .venv`
   `.venv\\Scripts\\activate`

   macOS/Linux:
   `python3 -m venv .venv`
   `source .venv/bin/activate`

4. Install dependencies:
   `pip install -r requirements.txt`
5. Optional: copy `.env.example` to `.env` and add your own API key. Keep `.env` private; never commit it.
6. Launch:
   `streamlit run app.py`

The app works without an API key using a transparent keyword-based demo fallback. The fallback is not an AI model and should be labelled as demo mode in any public demonstration.

## Suggested demo
1. Open Dashboard and show the synthetic risk overview.
2. Go to Assess Evidence.
3. Select Identity and Access Management > User access recertification.
4. Load `iam_access_review.txt`.
5. Run assessment and review evidence observed, potential gaps and follow-up questions.
6. Download the JSON assessment.
7. Repeat with `vulnerability_report.txt`.

## Suggested weekend build sequence
- Session 1: install Python, create environment, run the app.
- Session 2: explore the control library and synthetic evidence.
- Session 3: configure API key if available and run LLM assessment.
- Session 4: test at least five evidence cases, correct prompt issues, capture screenshots.
- Session 5: publish a short demo and GitHub README.

## Known limitations
- PDF support extracts selectable text; scanned PDFs need OCR, which is not included.
- No RAG, authentication, role-based access, encryption-at-rest, audit logging or production controls.
- No formal model evaluation or validated risk scoring.
- The demo-mode keyword rules are illustrative only.
- Do not use the output as an audit opinion or regulatory compliance determination.

## Portfolio positioning
Describe this as: "Built an experimental GenAI-powered IT Audit Copilot using Python and Streamlit to support evidence triage, control mapping, preliminary risk observations and human-reviewed audit documentation using synthetic banking scenarios."
