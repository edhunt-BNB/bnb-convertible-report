# Butternut Box D2MS Report Generator

Pulls data from Airtable (Base `appc3AWUlFaHlmdWk`, Table `tblkhYU7kDPoA6V23`) and generates 3 HTML reports + index hub page.

## Reports

- **NI Dispositions** — All NI records with 5 talk-time tiers (Critical/Review/Short/Medium/Long)
- **Callback Dispositions** — All CALLBACK records with 3 tiers (Short/Medium/Long)
- **Other Convertibles** — Remaining Convertible records by result code (TOOEXP, PAYISSUE, FUSSY, MEDIFOOD, HEALTH)

## Usage

```bash
AIRTABLE_PAT=pat... python3 generate_reports.py
```

Reports are written to `docs/`.

## Automation

GitHub Actions workflow runs daily at 9am London time. Set `AIRTABLE_PAT` as a repository secret.
