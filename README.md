# dustoff-dev

Opinionated log housekeeping tool with dry-run support

## Install

```bash
pip install -r requirements.txt
python -m logwash --help
```

## Usage

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## What it does

- Dry-run mode shows what would happen, touches nothing
- Archive matched logs into a timestamped .tar.gz
- Scan directories for log files by glob pattern
- Exit codes friendly for cron and CI
- Filter by age (--older-than) or size (--larger-than)

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── development.md
│   ├── faq.md
│   └── roadmap.md
├── examples/
│   └── quickstart.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   ├── cli.py
│   ├── errors.py
│   └── utils.py
├── tests/
│   └── test_cli.py
├── .gitignore
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
├── pyproject.toml
└── requirements.txt
```

## License

MIT licensed, see LICENSE.
