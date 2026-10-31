# DriftGuard-FYP-Self-Healing-CI-CD-Pipeline
An automated GitOps engine for CMP6200 that enforces "Code-as-Law" compliance. Detects AWS drift via custom Python state parsing, runs TFLint, Trivy, and Checkov security scans, dynamically generates Terraform code, and opens GitHub PRs (gh) for deterministic state synchronization.
