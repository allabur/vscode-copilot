---
mode: "agent"
tools: ["vscode", "terminal"]
description: "Set up complete CI/CD pipeline with automated testing and deployment"
---

# Setup CI/CD Pipeline

Create a comprehensive CI/CD pipeline for the current project with automated testing, security scanning, and deployment.

## Project Configuration
- **Platform**: ${input:platform:Choose CI/CD platform (github-actions, gitlab-ci, jenkins, azure-devops)}
- **Target Environment**: ${input:environment:Target deployment environment (aws, azure, gcp, docker, kubernetes)}
- **Application Type**: ${input:appType:Application type (web-app, api, microservice, mobile-app)}

## Pipeline Requirements

### Pipeline Stages
1. **Code Quality & Linting**
2. **Unit Testing**
3. **Integration Testing**
4. **Security Scanning**
5. **Build & Package**
6. **Deployment (Staging)**
7. **End-to-End Testing**
8. **Production Deployment**
9. **Post-Deployment Monitoring**

### Automated Testing Strategy
- Unit tests with coverage reporting
- Integration tests for API endpoints
- Security vulnerability scanning
- Dependency security checks
- Code quality analysis (SonarQube, CodeClimate)
- Performance testing for critical paths

### Deployment Strategy
- Blue-green deployment for zero downtime
- Automated rollback on failure
- Health checks and readiness probes
- Database migration handling
- Environment-specific configuration management
- Secret management and rotation

## Security Integration
- Static Application Security Testing (SAST)
- Dynamic Application Security Testing (DAST)
- Container image vulnerability scanning
- Dependency security scanning
- Infrastructure security validation
- Compliance checks and reporting

## Monitoring and Observability
- Application performance monitoring
- Error tracking and alerting
- Log aggregation and analysis
- Infrastructure monitoring
- Business metrics tracking
- SLA/SLO monitoring

## Pipeline Configuration Files

### GitHub Actions (.github/workflows/ci-cd.yml)
```yaml
name: CI/CD Pipeline
on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '18'
          cache: 'npm'
      - run: npm ci
      - run: npm run test:coverage
      - run: npm run lint
      - run: npm run type-check
```

### Docker Configuration
- Multi-stage Dockerfile for optimized images
- Docker Compose for local development
- Container security best practices
- Health check implementation
- Non-root user configuration

### Kubernetes Deployment
- Deployment manifests with proper resource limits
- Service and Ingress configurations
- ConfigMaps and Secrets management
- Horizontal Pod Autoscaler setup
- Network policies for security

## Environment Management
- Development environment setup
- Staging environment configuration
- Production deployment strategy
- Environment variable management
- Database migration strategies
- Feature flag implementation

## Quality Gates
- Code coverage thresholds (minimum 80%)
- Security scan passing requirements
- Performance benchmark requirements
- Manual approval for production
- Automated rollback triggers
- Compliance validation checkpoints

## Notification and Reporting
- Slack/Teams integration for build notifications
- Email alerts for deployment failures
- Dashboard for pipeline metrics
- Deployment history and audit logs
- Performance trend reporting
- Security scan result summaries

## Documentation
Generate comprehensive documentation:
1. **Pipeline Architecture Diagram**
2. **Deployment Process Documentation**
3. **Troubleshooting Guide**
4. **Environment Setup Instructions**
5. **Security and Compliance Report**
6. **Rollback Procedures**

## Deliverables
1. Complete CI/CD pipeline configuration files
2. Dockerfile and container configurations
3. Kubernetes deployment manifests (if applicable)
4. Testing strategy implementation
5. Monitoring and alerting setup
6. Documentation and runbooks
7. Security scanning configuration
8. Environment management scripts

Reference the [DevOps Guidelines](../instructions/devops.instructions.md) for additional best practices.

Generate a production-ready CI/CD pipeline following industry standards and security best practices.
