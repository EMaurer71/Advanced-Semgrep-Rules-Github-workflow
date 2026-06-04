Advanced Semgrep Rules & GitHub Workflow
This project contains my advanced, production‑grade Semgrep rule packs and a GitHub Actions workflow designed to detect AI‑specific security vulnerabilities across ML pipelines, notebooks, model‑serving code, and data engineering components.

It expands on the concepts introduced in Module 2 of the Coursera course Secure AI Code & Libraries with Static Analysis and demonstrates how to build a scalable, automated AI security scanning pipeline.

The repository includes:

A full suite of AI‑focused Semgrep rules

A GitHub Actions workflow that runs Semgrep on every push/PR

A demonstration notebook showing how the rules behave

A unified semgrep.yml configuration for bundling rule packs

This project is structured to mirror how real AI security engineering teams build and maintain Semgrep‑based detection systems.

📘 Notebook Included
Semgrep Demo Notebook
File: notebooks/semgrep_demo.ipynb

This notebook demonstrates:

How Semgrep loads custom rule packs

How rules fire on vulnerable ML code

How autofix rules apply patches

How to interpret Semgrep findings

How to run Semgrep locally and in CI

It includes examples of:

Unsafe model loading

Data poisoning vectors

Hardcoded secrets

Path traversal

Notebook‑specific vulnerabilities

Model integrity issues

Insecure model‑serving APIs

This notebook is the interactive companion to the rule packs.

📁 GitHub Actions Workflow
Folder: .github/workflows/

security_scan.yaml
This workflow:

Runs Semgrep using the advanced rule packs

Scans Python files, notebooks, and config files

Uploads SARIF and JSON reports

Blocks PRs on high‑severity findings

Mirrors enterprise‑grade CI/CD security pipelines

It demonstrates how to integrate AI‑specific static analysis into continuous delivery workflows.

📁 Advanced Semgrep Rule Packs
Folder: rules/

This project includes 11 specialized rule packs, each targeting a different AI security domain.

1. AI Secret Detection Rules
ai_secret_detection_rules.yml  
Detects API keys, tokens, credentials, and secrets commonly embedded in ML pipelines.

2. Autofix Rules
autofix_rules.yml  
Provides automated code fixes for common ML security issues.

3. Command Injection Rules
command_injection_rules.yml  
Detects unsafe shell execution patterns in data pipelines and training scripts.

4. Data Poisoning Rules
data_poisoning_rules.yml  
Identifies insecure data ingestion and preprocessing patterns.

5. ML CWE Mappings
ml_cwe_mappings.yml  
Maps AI‑specific vulnerabilities to CWE categories for reporting.

6. ML Pipeline Rules
ml_pipeline_rules.yml  
Detects insecure training, evaluation, and preprocessing code.

7. Model Integrity Rules
model_integrity_rules.yml  
Flags unsafe model loading, serialization, and provenance issues.

8. Model Serving API Rules
model_serving_api_rules.yml  
Detects insecure inference endpoints and over‑permissive APIs.

9. Notebook Security Rules
notebook_security_rules.yml  
Scans .ipynb files for:

Hidden secrets

Unsafe imports

Dangerous execution patterns

10. Path Traversal Rules
path_traversal_rules.yml  
Detects user‑controlled file paths in ML pipelines.

11. Unified Semgrep Config
semgrep.yml  
A single configuration file that bundles all rule packs for CI and local scanning.

📂 Folder Structure
Code
Advanced-Semgrep-Rules-Github-workflow/
├── .github/workflows/
│   └── security_scan.yaml
│
├── notebooks/
│   └── semgrep_demo.ipynb
│
└── rules/
    ├── ai_secret_detection_rules.yml
    ├── autofix_rules.yml
    ├── command_injection_rules.yml
    ├── data_poisoning_rules.yml
    ├── ml_cwe_mappings.yml
    ├── ml_pipeline_rules.yml
    ├── model_integrity_rules.yml
    ├── model_serving_api_rules.yml
    ├── notebook_security_rules.yml
    ├── path_traversal_rules.yml
    └── semgrep.yml
🧠 Why This Project Matters
AI systems introduce vulnerabilities that traditional static analysis tools cannot detect.
This project demonstrates how to build a custom AI‑focused static analysis engine using Semgrep.

It enables:

Early detection of ML‑specific vulnerabilities

Automated remediation via autofix rules

Notebook scanning

CI/CD enforcement

CWE‑aligned reporting

Secure ML pipeline development

This is the kind of tooling used by real AI security engineering teams.
