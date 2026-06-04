README — Advanced Semgrep Rules (Educational Overview)
Location:
Advanced-Semgrep-Rules-Github-workflow/rules/README.md

Advanced Semgrep Rules — Educational Overview
This folder contains a collection of AI‑specific Semgrep rule packs designed to detect vulnerabilities unique to machine learning pipelines, model‑serving systems, and notebook‑based development workflows.

These rules go beyond traditional static analysis by targeting:

ML pipeline weaknesses

Unsafe model loading

Data poisoning vectors

Notebook‑specific security issues

Model integrity risks

AI‑specific CWE mappings

Insecure inference APIs

Each rule pack is written to be readable, teachable, and extensible, making this directory a learning resource for anyone studying AI security static analysis.

📘 Educational Purpose of Each Rule Pack
Below is a breakdown of each rule pack and the vulnerability class it teaches.

1. AI Secret Detection Rules
File: ai_secret_detection_rules.yml

What it teaches:  
Secrets often leak into ML pipelines through notebooks, config files, or training scripts.
This rule pack demonstrates how to detect:

API keys

Cloud tokens

Hardcoded credentials

Model registry passwords

Why it matters:  
AI teams frequently prototype in notebooks, making secret leakage extremely common.

2. Autofix Rules
File: autofix_rules.yml

What it teaches:  
Semgrep can automatically rewrite insecure code.
This pack demonstrates:

How autofix patches are structured

How to replace unsafe patterns with secure alternatives

How to enforce secure defaults in ML pipelines

Why it matters:  
Autofix is essential for large ML teams where manual remediation is too slow.

3. Command Injection Rules
File: command_injection_rules.yml

What it teaches:  
ML engineers often use os.system, subprocess, or shell commands for:

Data preprocessing

Model conversion

Training orchestration

This pack detects unsafe shell execution patterns.

Why it matters:  
Command injection is one of the most common ML pipeline vulnerabilities.

4. Data Poisoning Rules
File: data_poisoning_rules.yml

What it teaches:  
Data ingestion is the largest attack surface in ML systems.
This pack detects:

Unvalidated input flows

Direct user‑controlled data ingestion

Unsafe preprocessing logic

Why it matters:  
Poisoned data can compromise training, evaluation, or inference.

5. ML CWE Mappings
File: ml_cwe_mappings.yml

What it teaches:  
AI vulnerabilities do not map cleanly to traditional CWE categories.
This pack provides:

AI‑specific CWE mappings

Educational examples

A taxonomy for ML security issues

Why it matters:  
Security reports require CWE alignment for industry compliance.

6. ML Pipeline Rules
File: ml_pipeline_rules.yml

What it teaches:  
ML pipelines contain unique risks such as:

Unsafe feature extraction

Insecure data loaders

Dangerous preprocessing steps

Unvalidated transformations

This pack detects these patterns.

7. Model Integrity Rules
File: model_integrity_rules.yml

What it teaches:  
Model files can be weaponized.
This pack detects:

Unsafe pickle loading

Missing signature verification

Untrusted model sources

Insecure serialization formats

Why it matters:  
Model integrity is a core AI security principle.

8. Model Serving API Rules
File: model_serving_api_rules.yml

What it teaches:  
Inference APIs often expose:

Over‑permissive endpoints

Debug routes

Unsafe input handling

Excessive model metadata

This pack detects insecure serving patterns.

9. Notebook Security Rules
File: notebook_security_rules.yml

What it teaches:  
Notebooks introduce unique risks:

Hidden secrets

Unsafe imports

Arbitrary code execution

Dangerous magic commands

This pack scans .ipynb files directly.

10. Path Traversal Rules
File: path_traversal_rules.yml

What it teaches:  
ML pipelines often load:

Models

Datasets

Config files

This pack detects user‑controlled file paths that could lead to traversal attacks.

11. Unified Semgrep Config
File: semgrep.yml

What it teaches:  
How to bundle multiple rule packs into a single configuration for:

Local scanning

CI/CD pipelines

Notebook scanning

ML pipeline scanning

🧠 Why These Rules Matter (Educational Summary)
AI systems introduce vulnerabilities that traditional static analysis tools cannot detect.
These rule packs teach:

How to design AI‑specific detection logic

How to map ML vulnerabilities to CWE categories

How to scan notebooks and pipelines

How to enforce secure model loading

How to detect data poisoning risks

How to build enterprise‑grade Semgrep configurations

This folder is both a toolkit and a learning resource.
