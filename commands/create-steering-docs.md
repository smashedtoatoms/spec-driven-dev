---
description: Creates steering documents that give your agent persistent knowledge about your project
allowed-tools: Read(*), Write(*), Edit(*), MultiEdit(*), TodoWrite
---

# Steering Files Creation Request
- Steering documents that give your AI Agent persistent knowledge about your project
- Create comprehensive steering rules for this repository.
- Do not refer to `agents` directory to create steering documents. Only use the project files.
- Copy AGENTS.md from the current project root to `agents/AGENTS.md`
- Analyze the repository and Please create three steering files under `agents/steering` directory:

1. product.md - Overview of the product, its features, and target audience
2. tech.md - Technical stack, development guidelines, and best practices
3. structure.md - Project structure, architecture patterns, and organization

Each file should be concise yet comprehensive, focusing on information that would be most useful for an LLM application operating in this project.
