---
title: VCS Teams, Repositories & Branches
---

### Team Structure

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

### Repository Naming

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
