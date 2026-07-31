# Task 1 - Deploy & Harden the Workload

## Objective

Deploy the `ledger-api` application on Kubernetes and harden it using production-grade security practices.

---

## Implemented Features

### Kubernetes Resources

- Namespace (`payments`)
- Deployment (`ledger-api`)
- Service (`ClusterIP`)
- ConfigMap
- Ingress
- Neighbour service (`reporting`)
- Dedicated ServiceAccount
- Least-Privilege RBAC

---

## Security Hardening

Implemented the following production-grade security controls:

- Containers run as a non-root user
- Read-only root filesystem
- Dropped all Linux capabilities
- RuntimeDefault seccomp profile
- Resource requests and limits
- Liveness probe
- Readiness probe

---

## Secrets Management

Plaintext secrets are intentionally excluded from version control.

For production deployments, secrets should be managed using one of the following:

- Bitnami Sealed Secrets
- External Secrets Operator
- SOPS-age

---

## Admission Control

A Kyverno policy (`policies/require-nonroot.yaml`) has been included to enforce that workloads run as non-root.

---

## Validation

The deployment was verified successfully.

Validation performed:

- Pods Running
- Deployment Available
- Service Created
- Ingress Created
- Health endpoint verified (`/health`)

---

## Screenshots

Screenshots demonstrating the deployment and health checks are included in the repository.

