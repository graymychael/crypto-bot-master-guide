# GitHub Actions Setup

## Workflow Example
```yaml
name: Run Crypto Bot

on:
  push:
    branches: [ main ]

jobs:
  run-bot:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-python@v4
        with:
          python-version: 3.10
      - run: pip install -r requirements.txt
      - run: python gui/crypto_bot_gui.py
```

## Deployment
Place this file at `.github/workflows/bot-deploy.yml`
