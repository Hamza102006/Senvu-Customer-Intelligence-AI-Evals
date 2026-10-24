# SafeVision AI — Customer Intelligence & AI Evals Platform

Portfolio upgrade of the original Customer Feedback ETL Pipeline.

## What it demonstrates
- Python ETL for CSV/JSON feedback
- Supabase/PostgreSQL multi-company data model
- VADER + TextBlob baselines
- 100-case AI evaluation suite across 20 failure modes
- Custom product-quality rubric and regression tracking
- Next.js dashboard starter for customer intelligence, evals, and human review

## Free-first setup
You can run the core project for $0. Leave `OPENAI_API_KEY` blank. VADER, TextBlob, ETL, tests, eval framework, Next.js locally, and local Supabase/PostgreSQL do not require paid AI credits.

## Quick start
```bash
python -m venv .venv
# Windows: .venv\Scripts\Activate.ps1
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env   # Windows PowerShell: Copy-Item .env.example .env
pytest -q
python -m ai.pipelines.ingest sample_data/legacy_feedback.csv
python -m ai.evals.run_evals --approach vader
python -m ai.evals.run_evals --approach textblob
```

See `docs/BUILD_GUIDE.md` for the step-by-step build plan.
