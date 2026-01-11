# CI DevSecOps Pipeline Notes

## Goal
Automate build, test, security scan, Docker build, and push.

---

## Pipeline Stages
1. Checkout
2. Build
3. Lint
4. SAST scan
5. Dependency scan
6. Unit tests
7. Docker build
8. Image scan (Trivy)
9. Runtime test
10. Push to DockerHub

---

## DevSecOps Concepts
- Shift-left security
- Immutable artifacts
- Quality gates
- Secrets management