# Task 2 – Secure CI/CD Pipeline & Supply Chain

## Objective

The objective of this task was to implement a production-oriented DevSecOps pipeline that automatically builds the application and performs security scanning before publishing the container image.

---

## Workflow Overview

The GitHub Actions workflow performs the following steps:

1. Checkout repository
2. Configure Python environment
3. Install application dependencies
4. Perform Static Application Security Testing (Semgrep)
5. Perform Secret Scanning (Gitleaks)
6. Perform Trivy Filesystem Scan
7. Build Docker image
8. Perform Trivy Image Scan
9. Push image to GitHub Container Registry (GHCR)
10. Upload security reports

---

## Security Controls

### Semgrep

Static Application Security Testing (SAST)

Detects:

- Insecure coding patterns
- Misconfigurations
- OWASP Top 10 issues

---

### Gitleaks

Scans the repository for accidentally committed:

- Passwords
- Tokens
- Secrets
- API Keys

A SARIF report is generated during the workflow.

---

### Trivy

Filesystem Scan

- Dependency vulnerabilities
- Misconfigurations

Image Scan

- Operating system vulnerabilities
- Package vulnerabilities
- High/Critical CVEs

---

## Reports

Generated reports:

- trivy-fs-report
- trivy-image-report
- gitleaks-results.sarif

Reports are available under:

```
Task2/reports
```

---

## Screenshots

Workflow execution screenshots are available in:

```
Task2/screenshots
```

---

## Outcome

The GitHub Actions workflow successfully:

- Built the Docker image
- Published the image to GHCR
- Executed Semgrep
- Executed Gitleaks
- Executed Trivy filesystem scan
- Executed Trivy image scan
- Generated security reports
