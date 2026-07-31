# Dodo Payments – DevSecOps Assignment

## Overview

This repository contains my submission for the Dodo Payments DevSecOps assignment.

The assignment focuses on deploying and securing a Kubernetes workload, implementing a secure CI/CD pipeline, and following DevSecOps best practices.

Due to the limited implementation time, I prioritized completing **Task 1** and **Task 2** with production-oriented configurations, validation, documentation, and screenshots instead of partially implementing all four tasks.

---

# Repository Structure

```
.
├── .github/
│   └── workflows/
├── Task1/
├── Task2/
├── Task3/
├── Task4/
└── README.md
```

---

# Task 1 – Deploy & Harden the Workload

Implemented:

- Kubernetes Deployment
- Service
- ConfigMap
- Secret
- ServiceAccount
- RBAC (Role & RoleBinding)
- Ingress
- Security Context
  - Non-root user
  - Read-only root filesystem
  - Dropped Linux capabilities
  - RuntimeDefault seccomp profile
- Resource Requests & Limits
- Liveness & Readiness Probes
- Kyverno admission policy
- Documentation
- Validation screenshots

Documentation:

```
Task1/README.md
```

---

# Task 2 – Secure CI/CD Pipeline

Implemented:

- GitHub Actions workflow
- Docker image build
- GHCR image publishing
- Semgrep (SAST)
- Gitleaks (Secret Scanning)
- Trivy Filesystem Scan
- Trivy Image Scan
- Security Reports
- SARIF report generation

Documentation:

```
Task2/README.md
```

---

# Task 3 – Service Mesh & Zero Trust

Not implemented due to time constraints.

Planned implementation:

- Istio Service Mesh
- mTLS (STRICT)
- AuthorizationPolicy
- NetworkPolicy
- Zero Trust communication

---

# Task 4 – Offensive Security Assessment

Not implemented due to time constraints.

Planned implementation:

- Reconnaissance
- Vulnerability Assessment
- CVE Identification
- Proof of Concepts
- Penetration Testing Report

---

# Technologies Used

- Kubernetes
- Docker
- GitHub Actions
- GitHub Container Registry (GHCR)
- Semgrep
- Trivy
- Gitleaks
- Kyverno

---

# Notes

The focus of this submission was **quality over quantity**.

Rather than partially implementing every task, I completed the Kubernetes hardening and DevSecOps pipeline end-to-end, validated the implementation, and documented the approach with screenshots and reports.
