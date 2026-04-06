# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a **Chinese-language value investing research repository**. It contains structured methodology files ("skills") for researching publicly listed companies, and the resulting research notes. The framework draws heavily from Buffett, Munger, Duan Yongping (段永平), and Tang Chao's (唐书房) value investing principles.

## Language

All content is in **Chinese (Simplified)**. Research notes, skill files, templates, and all interactions should be in Chinese unless the user requests otherwise.

## Repository Structure

### Skills (methodology framework)
- `skills/skill_v2.md` — **Primary research skill (v3)**. The definitive 10-step research process for deep company analysis. ~1500 lines. Always use this version, not `skill.md` (v1, deprecated).
- `skills/skill_tracking.md` — **Tracking skill**. Downstream continuation of skill_v2 for ongoing monitoring of portfolio/watchlist companies after initial research.
- `skills/模板.md` — **Research note template**. The structured template that matches skill_v2's output format. Use when creating new research notes.
- `skills/财务报表分析.md` — **Financial statement analysis skill**. Supplementary framework focused on reading financial reports through a value investing lens.

### Research Notes (output)
Files at the repository root follow the naming convention: `公司名_股票代码_研究笔记.md` or `_v2.md` for updated versions. Examples:
- `快手_1024_研究笔记_v2.md` (Kuaishou, HKEX:1024)
- `永新股份_002014_研究笔记_v2.md` (Yongxin, SZSE:002014)
- `赛轮轮胎_601058_研究笔记.md` (Sailun Tire, SHSE:601058)
- `乐舒适_02698_研究笔记_v2.md` (HKEX:02698)

Tracking notes follow: `公司名_代码_跟踪笔记_事件.md`

## How to Use the Skills

### For new company research
1. Follow `skills/skill_v2.md` step-by-step (Step 0 through Step 10)
2. Use `skills/模板.md` as the output template
3. Create a new research note file at the repo root following the naming convention

### For ongoing tracking of researched companies
1. Follow `skills/skill_tracking.md`
2. Reference the company's existing research note as the baseline
3. Create a tracking note file

## Research Process Overview (skill_v2.md)

The 10-step process with **four veto gates** (steps 1, 6, 7, 8):

1. **Step 0** — Circle of competence self-check (user must answer; AI cannot judge this)
2. **Step 1** — Junk company filter (one-vote veto) — veto gate 1
3. **Step 2** — Company overview & business description (facts only, no conclusions)
4. **Step 3** — Industry analysis (including growth logic checklist — the most critical analytical section)
5. **Step 4** — Business model & moat assessment
6. **Step 5** — Corporate culture & management evaluation
7. **Step 6** — Deep financial analysis (10-year data, red line checks) — veto gate 2
8. **Step 7** — Investment value verification (4 core questions, 3 prerequisites) — veto gate 3
9. **Step 8** — Risk & inversion test (bear case audit, Munger pre-mortem) — veto gate 4
10. **Step 9** — Valuation (Tang Chao's simplified DCF: ideal buy price = year-3 net profit × reasonable PE / 2)
11. **Step 10** — Monitoring checklist generation

### Key Valuation Method: "Tang Chao Method" (老唐估值法)
- Ideal buy price = estimated year-3 net profit × reasonable PE (15-25x) ÷ 2
- Sell trigger: market cap ≥ 150% of 3-year合理估值, or PE > 50x
- Prerequisites: profits are real, sustainable, and don't require heavy reinvestment

## Data Source Priority

For **A-shares**: 东方财富/同花顺F10 > 巨潮资讯网年报PDF > 新浪财经 > 亿牛网 > English sites (fallback only)

For **Hong Kong stocks**: 港交所披露易PDF > 东方财富港股/同花顺港股 > Yahoo Finance > English sites (fallback only)

Never use low-precision English data sources (SimplyWallSt, StockAnalysis) for A-share/HK companies when Chinese sources are available.

## Data Handling Rules

When data is unavailable, use this three-tier marking system:
- **确认值** — From annual reports or authoritative sources. Use directly with source citation.
- **~估算值** — From non-primary sources. Prefix with `~` and note the estimation method.
- **"公司未披露"** — Confirmed not publicly available. Mark as such (not "待补充") to avoid wasted re-searching.

## AI Boundary Declaration

AI assists with data gathering, structured analysis, and cross-validation. AI **cannot** judge: circle of competence boundaries, management character, or make final buy/sell decisions. When AI conclusions feel wrong, the user should trust their intuition and re-examine.
