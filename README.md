# PeerShield — Misconception Intelligence Lab

**A working, browser-based prototype for identifying possible misconceptions in peer learning, visualizing exposure links, and coordinating faculty-reviewed corrective learning.**

## Problem statement

Peer-learning platforms connect students, but an incorrect explanation can be repeated in subsequent learning sessions. Standard matching and messaging features do not necessarily identify recurring conceptual errors or provide targeted correction. How can a peer-learning system flag possible shared misconceptions, inspect relevant learning links without assigning blame, and verify that corrective learning worked?

## Proposed solution

PeerShield combines a rule-based concept quiz, a peer learning network graph, a human review queue, and a targeted reassessment workflow. It is a **synthetic-data educational prototype**, not a production-ready AI system.

## Features

- Responsive, animated dashboard with metrics and event timeline
- Interactive Python fundamentals assessment with three questions
- Predefined misconception detection (assignment vs equality, list indexing, Boolean operators)
- Interactive eight-student peer network graph
- One-click scenario that introduces four fictional misconception signals
- Faculty review: approve correction or dismiss a signal
- Personalized correction and a follow-up understanding check
- Persistent demo state via browser `localStorage`
- JSON report export and one-click demo reset
- Runs on GitHub Pages; no API keys or server needed

## Run locally

Download the repository, extract it, and open `index.html` in a modern browser. Or use VS Code's Live Server extension.

## Deploy to GitHub Pages

1. Create a **public** GitHub repository.
2. Upload `index.html`, `style.css`, `script.js`, and `README.md` to the repository **root**.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, and click **Save**.
5. After deployment completes, open the published site URL shown in Pages settings.

## Demo script (2–3 minutes)

1. On **Overview**, click **Simulate misconception spread**.
2. Open **Learning Network** and inspect the highlighted students and links.
3. Open **Faculty Review** and approve two signals, dismiss another.
4. Open **Recovery Studio**, read the correction, answer a follow-up question, and see the recovered count change.
5. Open **Assessment Lab**, take the quiz for a learner, and inspect any new signals.
6. Return to Overview and export the JSON report.

## Architecture

```text
HTML + CSS + JavaScript
        |
        +-- Assessment engine (fixed validated answer key)
        +-- Misconception signals (predefined answer patterns)
        +-- Learning graph (fictional peer-to-peer links)
        +-- Faculty review (human approval/dismissal)
        +-- Recovery studio (concept correction + reassessment)
        +-- localStorage (browser-only persistence)
```

## Limitations and responsible interpretation

- All learner names, peer links, and scenario records are **fictional**.
- Incorrect answers are **signals**, not proof of misinformation transmission.
- Shared errors cannot establish which mentor caused them.
- This is **not machine learning**; it uses deterministic answer rules.
- Faculty review is simulated in the same browser; there is no login, real access control, server, or multi-device synchronization.
- Real deployments would require informed consent, privacy protections, secure authentication, validated assessments, fairness testing, and educator oversight.
- The three-question demo is not sufficient for formal learning evaluation.

## Suggested future extensions

Secure student accounts, MySQL/Flask backend, consent-based session records, educator-designed question banks, and longitudinal learning evaluation.

## Project type

College mini-project prototype · HTML, CSS, JavaScript · GitHub Pages compatible

**PeerShield: Learn together. Verify understanding. Correct with care.**
