---
title: Environments (AWS & CI/CD)
---

Status: Proposed

Standard Environment Names

Use the MHCLG Cloud Platform environment names throughout AWS accounts, GitHub Environments and CI/CD pipelines. Learn more about AWS account types on the intranet.

```
sandbox - Experimentation and proof-of-concept work.
ci - Automated build and deployment activities.
development - Feature development and integration.
test - Application and integration testing.
staging - Pre-production validation and assurance.
production - Live service delivery.
```

Avoid:

```
dev
uat
preprod
live
prod
```

AWS Account Naming

<project>-<environment>

Examples:

```
align-development
align-test
align-staging
align-production
```

GitHub Environment Naming

```
development
test [optional, if environment is in use]
staging
production
```

Deployment Model

Use a single deployable branch: 

```
main
```

Deployments are promoted through active environments:

```
main
  ↓
development
  ↓
test [optional, if environment is in use]
  ↓
staging
  ↓
production
```

Avoid environment-specific branches such as:

```
development
test
staging
production
```


2. VCS Teams, Repositories & Branches

Team Structure

Projects are the ownership and permission boundary.

```
<project>
```

```
<project>-devops
<project>-eng
<project>-read
```

Examples:

```
align
align-devops
align-eng
align-read
```

This allows simple onboarding and least-privilege access:

Add contractor

```
→ align-devops
```

Repository Naming

Repositories represent technical assets.
Preferred naming:

```
<project>-<component>
```

Examples:

```
align-api
align-ui
align-infrastructure
align-architecture
```

Existing repositories do not require renaming. Team ownership should be used to manage access rather than repository naming conventions.
