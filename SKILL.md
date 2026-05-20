# Weekly Reporter

> **Agent**: `depositback-agent-weekly-reporter`  
> **Group**: Analytics  
> **Product**: DepositBack — Security Deposit Demand Letter Service

## Purpose

Generates: unique visitors by UTM, visitor→form→purchase CVR, revenue, refund rate, TikTok/Instagram engagement, SEO clicks, AI citation check. Monthly: channel ROI, content audit, funnel analysis, A/B results, competitive check, GEO tracking.

## DepositBack Context

DepositBack is a single-page, no-signup transactional product for US renters seeking to recover security deposits. The entire customer journey fits on one URL: landing page → 6-question form → Revolut payment → PDF emailed. Conversion rate target: **4% visitor-to-purchase minimum**.

## Inputs

- Funnel data from funnel-analyst
- Channel scores from channel-scorer
- Attribution from utm-tracker

## Outputs

- Weekly report markdown → operations/dashboard
- Monthly deep-dive → operations/strategy

## Human Escalation Points 🛑

- Revenue target misses
- Conversion rate <4% for 2+ weeks
- Refund rate >10%

## Skills

| Skill | Description | Status |
|-------|-------------|--------|
| `noop` | Health check / pipeline verification | ✅ Active |
| `execute` | Primary function for this agent | 🔧 Planned |

## Workflow

1. Poll `data/inbox/` for task manifests from upstream agents.
2. Resolve required skills (local `skills/` or ClawHub fallback).
3. Execute workflow.
4. Write artifacts to `data/outbox/`.
5. Update `data/state.json`.

## Runtime

```bash
pip install -r requirements.txt
python runtime/main.py
```
