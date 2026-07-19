---
description: Ray cluster safety — do not kill root Ray processes
globs:
alwaysApply: true
---

# Ray Cluster Ops

When working on the cluster with Ray for resource management, job orchestration, task execution, or Python package installation:

- Do **not** kill the main / root Ray processes (`raylet`, GCS, dashboard, head/worker services).
- If cleanup is needed, only terminate **specific Ray jobs** selectively.
- Prefer job-scoped stop (`ray job stop`, cancel by job id) over process-level kills.
