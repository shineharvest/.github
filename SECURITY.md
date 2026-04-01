# Security Policy

## Reporting Vulnerabilities

Report security vulnerabilities to the `security-assurance` team through the private channel defined in the program security plan. **Do not open public issues for security vulnerabilities.**

If you are unsure whether an issue is security-relevant, err on the side of private reporting.

## Severity Classification

| Severity | Description | Response Time |
|----------|-------------|---------------|
| Critical | Beam transmission safety impact or loss of control integrity | Immediate (less than 1 hour) |
| High | Control system integrity at risk, unauthorized operational state change | Less than 4 hours |
| Medium | Data integrity or availability concern, policy deviation | Less than 24 hours |
| Low | Documentation gap, process improvement | Less than 1 week |

## Automatic Critical Classification

The following are automatically classified as Critical severity regardless of other factors:

- Any vulnerability enabling unauthorized beam activation
- Any vulnerability enabling beam redirection or spoofing
- Any vulnerability enabling generation state falsification
- Any compromise of safety interlock logic

## Detailed Security Guidance

For threat models, trust boundary definitions, hardening requirements, and security policies, refer to the `sh-security` repository.

## Security Contact

Escalate all security concerns to `@shineharvest/security-assurance`.
