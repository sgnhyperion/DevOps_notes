## 1. CI vs CD Recap

CI:
- Frequent code merges
- Automated builds & tests

CD:
- Automated deployments
- Minimal downtime releases

---

## 2. Kubernetes Setup for CI/CD

Requirements:
- At least 1-node cluster
- VM setup using Vagrant/VirtualBox
- Or cloud VM with pre-installed Kubernetes

---

## 3. GitHub Actions

Used for:
- Build
- Test
- Deploy

Workflows defined in YAML.

---

## 4. Self-Hosted (Custom) Runners

Instead of GitHub-hosted runners, use your own machine.

Benefits:
- More control
- Custom environments
- Access to private networks

Setup:
- Install runner
- Register using config.sh
- Add labels & permissions

---

## 5. Testing Environments

SIT (System Integration Testing)
Performance Testing
Security Testing

Automating tests reduces human error.

---

## 6. Practical Learnings
- CI and CD can be separate
- Pipelines must match app needs
- Team collaboration is important
- Individual accountability in projects