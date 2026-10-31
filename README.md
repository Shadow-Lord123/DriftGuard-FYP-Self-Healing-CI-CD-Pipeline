# DRIFT-GUARD: Self-Healing CI-CD Pipeline

A strict "Code-as-Law" GitOps pipeline and automated remediation engine built for CMP6200[cite: 1]. Designed to eliminate unauthorized cloud infrastructure drift (ClickOps) through automated state scanning, multi-framework security gates, and deterministic state synchronization.

## Key Features
* **Automated Drift Detection & Code Generation**: Parses live Terraform state files via a custom Python engine (`drift_guard.py`) to catch manual environment changes and dynamically generate corresponding Terraform configuration updates.
* **Multi-Layer Security Scanning**: Integrates `TFLint`, `Tfsec`, and `Checkov` into GitHub Actions to enforce rigorous compliance before changes reach production.
* **Automated GitOps Remediation**: Dynamically generates and opens pull requests using the GitHub CLI (`gh`) when drift is identified.
* **Strict "Code-as-Law" Enforcement**: Enforces absolute adherence to declarative baseline state upon pull request closure, systematically purging unvetted manual hotfixes.
