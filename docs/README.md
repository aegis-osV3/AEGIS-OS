# AEGIS OS V3 Documentation Index

This documentation set is the canonical engineering guide for transferring, building, deploying, validating, operating, and extending AEGIS OS V3.

## Getting Started

- [Quick Start](getting-started/QUICK_START.md)
- [Installation Guide](getting-started/INSTALLATION_GUIDE.md)
- [Bootstrap Guide](getting-started/BOOTSTRAP_GUIDE.md)

## Repository And Architecture

- [Repository Guide](repository/REPOSITORY_GUIDE.md)
- [Repository Map](repository/REPOSITORY_MAP.md)
- [Architecture Overview](architecture/ARCHITECTURE_OVERVIEW.md)
- [API Documentation](API.md)

## Development

- [Developer Guide](development/DEVELOPER_GUIDE.md)
- [Build Reproducibility](development/BUILD_REPRODUCIBILITY.md)
- [Testing Guide](testing/TESTING_GUIDE.md)

## Deployment And Operations

- [Docker Guide](deployment/DOCKER_GUIDE.md)
- [Deployment Verification Guide](deployment/DEPLOYMENT_VERIFICATION_GUIDE.md)
- [Operations Guide](operations/OPERATIONS_GUIDE.md)
- [Health Check Guide](operations/HEALTH_CHECK_GUIDE.md)

## Configuration And Platform Support

- [Configuration Guide](configuration/CONFIGURATION_GUIDE.md)
- [Cross-Platform Guide](platform/CROSS_PLATFORM_GUIDE.md)

## Security And Troubleshooting

- [Security Guide](security/SECURITY_GUIDE.md)
- [Troubleshooting Guide](troubleshooting/TROUBLESHOOTING_GUIDE.md)
- [Documentation Standards](standards/DOCUMENTATION_STANDARDS.md)

## Omega 3 Evidence

- [Omega 3 Implementation Log](reports/omega3/OMEGA3_IMPLEMENTATION_LOG.md)
- [Engineering Audit Report](reports/omega3/ENGINEERING_AUDIT_REPORT.md)
- [Repository Quality Report](reports/omega3/REPOSITORY_QUALITY_REPORT.md)
- [Build Verification Report](reports/omega3/BUILD_VERIFICATION_REPORT.md)
- [Deployment Verification Report](reports/omega3/DEPLOYMENT_VERIFICATION_REPORT.md)
- [Security Scan Summary](reports/omega3/SECURITY_SCAN_SUMMARY.md)
- [Documentation Review](reports/omega3/DOCUMENTATION_REVIEW.md)
- [Transfer Readiness Assessment](reports/omega3/TRANSFER_READINESS_ASSESSMENT.md)
- [Gap Analysis](reports/omega3/GAP_ANALYSIS.md)
- [Release Notes](reports/omega3/RELEASE_NOTES.md)
- [Final Closure Status](reports/omega3/FINAL_CLOSURE_STATUS.md)

Generated Omega 3 verification reports are written to `docs/reports/omega3/` by:

```powershell
.\scripts\aegis.ps1 verify-platform
.\scripts\aegis.ps1 build-verify
.\scripts\aegis.ps1 verify-deployment
.\scripts\aegis.ps1 security-scan
.\scripts\aegis.ps1 omega3-closure
```
