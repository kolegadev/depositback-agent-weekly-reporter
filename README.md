# depositback-agent-weekly-reporter

Compiles the Monday 30-minute weekly review and monthly deep-dive

## DepositBack Agent Network — Analytics

Part of the DepositBack autonomous marketing system.

## Quick Start

```bash
git clone https://github.com/kolegadev/depositback-agent-weekly-reporter.git
cd depositback-agent-weekly-reporter
pip install -r requirements.txt
python runtime/main.py
```

## Structure

```
.
├── SKILL.md, manifest.json, README.md
├── runtime/main.py
├── skills/skill_resolver.py, noop.py
├── data/inbox/, data/outbox/
└── .github/workflows/heartbeat.yml, scan.yml
```

## License

MIT — DepositBack Agent Network
