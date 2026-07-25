---
name: Static-site runtime
description: Runtime setup for imported static sites served by a simple HTTP server.
---

When an imported static site expects a language runtime command that is missing from PATH, keep the existing server approach and invoke the runtime through the project's available Nix environment rather than restructuring the site.

**Why:** The imported workflow can reference a runtime that is not installed in the current environment even when the static site itself has no dependencies.

**How to apply:** First confirm the existing workflow command and project stack, then use the smallest workflow-only runtime adjustment needed to serve the existing entry point.