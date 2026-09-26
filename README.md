# 🛡️ Secret Guard

**Secret Leak & Zero-Day Early Warning System**

Secret Guard is a source-code security scanner that detects exposed secrets and suspicious code patterns before deployment.

## Features

- Secret/API key/password detection
- High-entropy unknown-secret detection
- Suspicious code heuristics
- Risk levels: Critical, High, Medium, Low
- Zero-Day Early Warning dashboard
- Recommended remediation
- Browser-based code analysis
- Paste code or upload a file
- HTML security reports
- Git pre-commit hook support
- Python standard library only

## Start the web application

Windows:

```powershell
python main.py web
```

Then open:

**http://127.0.0.1:8000**

Paste code or upload a source file and click **Analyze Code**.

## Command-line scan

```powershell
python main.py scan test_samples/vulnerable_demo.py --html demo_report.html
```

## Important limitation

The Zero-Day Early Warning feature is heuristic. It identifies suspicious/anomalous indicators that may deserve further investigation. It does **not** prove that a zero-day vulnerability exists.

## Architecture

Browser UI → Python HTTP server → Scanner Engine → Risk Analysis → Zero-Day Heuristics → Results Dashboard
