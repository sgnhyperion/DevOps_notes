## 1. What is CI/CD?

### Continuous Integration (CI)
CI is the practice of frequently merging code changes into a shared repository and automatically:
- Building the code
- Running tests
- Checking code quality

Goal:
Keep the main branch always in a deployable state.

---

### Continuous Deployment / Delivery (CD)
CD automates releasing applications.

Continuous Delivery:
- Code is always ready for release
- Deployment may require approval

Continuous Deployment:
- Every successful change is automatically deployed to production

---

## 2. Why CI/CD Matters
- Faster releases
- Early bug detection
- Reduced integration issues
- Better developer productivity
- Reliable deployments

---

## 3. DevSecOps
DevSecOps = DevOps + Security

Security is integrated at every stage:
- Secure coding practices
- Automated security scans
- Dependency checks
- Container scanning

Goal: “Shift security left” (earlier in pipeline).

---

## 4. GDPR (General Data Protection Regulation)
A data privacy law in the EU.

Key ideas:
- Protect user data
- Consent for data usage
- Right to delete data
- Secure storage & processing

Important for applications handling user data.

---

## 5. SAST vs SCA

### SAST (Static Application Security Testing)
- Scans source code
- Finds vulnerabilities early
Examples:
SQL injection risks, insecure code patterns

### SCA (Software Composition Analysis)
- Scans dependencies/libraries
- Detects known CVEs
Prevents supply chain attacks

---

## 6. Testing Types

### Unit Testing
Tests small pieces of code.
Fast and developer-focused.

### Integration Testing
Tests interaction between components.
Ensures modules work together.

---

## 7. Feature Flagging
Allows enabling/disabling features without redeploying.

Benefits:
- Safe rollouts
- A/B testing
- Quick rollback

---

## 8. Artifact Management Tools
Store build outputs (artifacts).

Examples:
- JFrog Artifactory
- Nexus
- GitHub Packages

Artifacts:
JARs, Docker images, binaries.

---

## 9. Dockerization
Packaging apps into containers.

Benefits:
- Consistent environments
- Easy deployment
- Portability

---

## 10. Waterfall vs DevOps

Waterfall:
- Linear stages
- Slow feedback

DevOps:
- Continuous cycles
- Fast feedback
- Automation

---

## 11. Linting
Analyzes code for style and errors.

Benefits:
- Cleaner code
- Fewer bugs
- Standardized style