<div align="center">

# 🔍 Website QA Skill

**A read-only agent skill that audits websites — it never edits them.**

[![Type](https://img.shields.io/badge/type-Agent%20Skill-6E56CF)]()
[![Mode](https://img.shields.io/badge/mode-read--only-2EA043)]()
[![Checklists](https://img.shields.io/badge/checklists-5-blue)]()
[![License](https://img.shields.io/badge/license-Proprietary-lightgrey)]()

</div>

---

Point it at a live site or web app and it runs a standard QA suite covering
**cybersecurity**, **Laravel/MySQL security & SEO**, **general front-end/back-end QA**,
**functionality**, **performance**, **mobile responsiveness**, **design**, and
**accessibility** — then hands back two clean, evidence-backed reports.

> 🛡️ **This skill is an auditor, not an editor.**
> It inspects and reports. It never touches your code, config, database, or infrastructure.

---

## 📋 Table of Contents

- [What it does](#-what-it-does)
- [Checklists covered](#-checklists-covered)
- [Hard rules](#-hard-rules)
- [Output](#-output)
- [Usage](#-usage)
- [Repo structure](#-repo-structure)
- [Core principle](#-core-principle)

---

## ⚙️ What it does

| Step | Description |
|---|---|
| **1. Scope** | Identifies target, project ID, tech stack, available access, and applicable checklists. |
| **2. Applicability** | Decides which checklist items actually apply — no gallery? Gallery checks are skipped, not failed. |
| **3. Test** | Runs every applicable item as a read-only check, backed by real, reproducible evidence. |
| **4. Verify** | Re-checks findings where practical to cut down false positives. |
| **5. Report** | Generates two files — an issue log and a passed-tests log. |
| **6. Summarize** | Gives a short pass/fail/N-A breakdown in chat, without dumping every checklist line. |

---

## ✅ Checklists covered

| Checklist | Tag | Applies when |
|---|:---:|---|
| 🛡️ Cybersecurity | `CYBER` | Always evaluated for applicability |
| 🔐 Laravel / MySQL Security | `LARAVEL-SEC` | Project confirmed to use Laravel/MySQL |
| 📈 Laravel / MySQL SEO | `LARAVEL-SEO` | Project confirmed to use Laravel/MySQL |
| 🧪 General QA | `GENERAL-QA` | Always evaluated for applicability |
| 🎨 Design & Accessibility | `DESIGN` | Always evaluated for applicability |

Only the checklists — and items within them — that genuinely apply to the target
are run. Irrelevant items are marked `N/A` with a reason: never silently skipped,
never force-failed.

---

## 🚫 Hard rules

**Never allowed**
- ❌ Modifying the target — no code, config, `.env`, database, permission, or infra changes, even if a fix looks obvious or is requested mid-run
- ❌ Brute-forcing, credential guessing, destructive scans, or DoS/resource-exhaustion testing

**Always required**
- ✅ Read-only checks only — GETs, header inspection, DevTools, non-destructive scanners, `composer audit` / `npm audit`, safe form inputs, authorized-credential access
- ✅ Every **Fail** backed by concrete, reproducible evidence (URL, status code, header, console error, etc.) — no vague findings
- ✅ Every **Pass** backed by observable proof, never "the framework probably handles it"
- ✅ Anything unverifiable with available access is marked `N/A` with a specific reason, never guessed

---

## 📄 Output

Every run produces two files in `/mnt/user-data/outputs/`:

| File | Contents |
|---|---|
| `Issue_Log_No_<x>.txt` | Every failed item — checklist, severity (`Critical`/`High`/`Medium`/`Low`), confidence (`High`/`Medium`/`Low`), observed behavior, evidence, and a general remediation recommendation. Historical logs are never overwritten; the run number auto-increments. |
| `Passed_Tests.txt` | Every passed item plus the N/A list with reasons. Regenerated fresh each run. |

🔒 Secrets are never reproduced in output — if one is found, only its type and location are reported.

---

## 🚀 Usage

Trigger it by asking your Antigravity agent to QA test, audit, review, or run the checklist against a site:

```
Run the QA checklist against https://example.com
QA test our staging site, project ID PROJ-1042
Audit example.com for cybersecurity and SEO only
```

If you don't specify a checklist, the skill inspects the target's stack and
functionality first, then selects applicable checklists automatically. Name a
checklist explicitly, and that's what runs.

---

## 📁 Repo structure

```
.
├── SKILL.md
└── references/
    ├── cybersecurity-checklist.md
    ├── laravel-mysql-security-checklist.md
    ├── laravel-mysql-seo-checklist.md
    ├── general-qa-checklist.md
    └── design-checklist.md
```

---

## 🎯 Core principle

> Accurate QA reporting, not maximum issue count.
> A smaller set of well-supported findings beats a long list of false positives.

**Determine applicability → test what applies → verify what it can → record evidence → report accurately → leave the target unchanged.**

---

<div align="center">

Made with ❤️ at **Sesame Technologies Pvt. Ltd.**

</div>
