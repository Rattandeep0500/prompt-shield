Prompt Shield

AI Prompt Security & Adversarial Testing Platform

Prompt Shield is a research-oriented security project focused on detecting and analyzing adversarial prompts, prompt injection, jailbreak patterns, prompt leakage, and data-exfiltration attempts against AI systems.

Current status: Basic research prototype — actively under development and will be expanded substantially over time.

Overview

Prompt Shield explores how a dedicated security layer can identify potentially malicious instructions before they can influence an AI system.

The current version provides a dashboard for:

Prompt scanning and threat classification

Threat scoring and technique identification

Prompt injection and jailbreak analysis

Controlled adversarial testing through an Attack Lab

Scan and simulation history

Analytics and reporting

Dataset export

AI model monitoring and management interface

This is the initial version of the project. The architecture, detection methods, evaluation framework, and model integrations will continue to evolve as development progresses.

Current Detection Areas

The current prototype focuses on several common attack families:

Direct prompt injection

Indirect prompt injection

Role-play / persona jailbreaks

Prompt leaking

Encoding and obfuscation

Context / format manipulation

Multi-turn escalation

Data-exfiltration attempts

The goal is not simply to flag suspicious text, but to provide an explanation of why an input may represent a security risk.

Attack Lab

The Attack Lab is designed to evaluate how an AI system responds to controlled adversarial probes.

It currently provides a framework for testing attack categories and producing a resilience assessment.

The longer-term goal is to expand this into a reproducible adversarial evaluation framework covering:

Different model families

Different attack strategies

Obfuscated and paraphrased attacks

Multi-turn attacks

RAG-based attacks

Tool-use and agentic attacks

Architecture

The project is currently centered around a browser-based security dashboard with a path toward a server-side analysis architecture:

User / Application
        │
        ▼
  Prompt Shield
      Scanner
        │
   ┌────┴─────┐
   ▼          ▼
Rule-based   Model-based
analysis     analysis
   │          │
   └────┬─────┘
        ▼
 Threat Assessment
        │
   ┌────┴─────┐
   ▼          ▼
Explanation  Risk Score
        │
        ▼
   Security Report

For production deployment, model credentials and privileged AI-system access will be kept behind a server-side API rather than exposed in the frontend.

Research Direction

A major goal of Prompt Shield is to move from a functional prototype toward measurable AI-security research.

Future evaluation will investigate metrics such as:

Precision

Recall

F1 score

False-positive rate

False-negative rate

Attack-family coverage

Model resilience

Performance against unseen attack variants

The project will also explore whether combining deterministic security rules with model-based analysis can improve detection performance without creating excessive false positives.

Development Roadmap

Completed

Security-focused dashboard

Prompt Scanner

Threat classification

Threat scoring

Attack Lab interface

Attack-vector taxonomy

Analytics

Reports

Dataset export

GitHub Pages deployment

In development

Production backend

Secure model/provider adapters

Persistent database

Authentication and authorization

Rate limiting

Reproducible adversarial dataset

Automated benchmark runner

Precision / recall / F1 evaluation

RAG injection testing

Agentic/tool-use security testing

Security regression tests

Important Note

Prompt Shield is currently a basic research prototype, not a production security product.

Detection results can contain false positives and false negatives. The project is being developed iteratively, with the intention of improving the detection engine, evaluation methodology, backend architecture, and attack coverage over time.

Live Demo

The current frontend is deployed through GitHub Pages:
https://rattandeep0500.github.io/prompt-shield/

Project Status

This repository represents the current development stage of Prompt Shield.

The project will continue to be updated over time as new detection techniques, evaluation methods, model integrations, and security capabilities are developed.

Security

See SECURITY.md for the project's security principles and responsible-testing guidance.

License

No open-source license has been selected yet. Until a license is added, default copyright restrictions apply.
