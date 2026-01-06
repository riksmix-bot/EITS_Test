# Cursor Rules & Prompts

A collection of **Cursor AI rules**, **agent configurations**, and **reusable commands** for building enterprise-grade applications. Designed for teams working with Java/Spring Boot backends and Nuxt/Vue frontends.

## What's Included

### 📋 Rules (`rules/`)

Cursor rules (`.mdc` files) that automatically apply coding standards, security practices, and conventions when editing code.

| Category | Rules | Description |
| :------- | :---- | :---------- |
| **Common** | `security.mdc`<br>`component-technical-standards.mdc`<br>`integration-standards.mdc` | Language-agnostic security best practices (OWASP), component design standards, and integration patterns |
| **Java** | `java-code-standards.mdc`<br>`application-logging.mdc`<br>`audit-logging.mdc`<br>`jooq-database-access.mdc` | Java 21+ code style, SLF4J logging conventions, audit trail patterns, and type-safe database access with jOOQ |
| **Spring Boot** | `spring-conventions.mdc`<br>`spring-retry-conventions.mdc`<br>`spring-testing.mdc` | Spring Boot patterns, resilience with retry/circuit breakers, and testing with TestContainers |

### 🤖 Agents (`agents/`)

`AGENTS.md` files that define AI assistant personas for specific tech stacks. These provide project-specific commands, boundaries, and workflows.

| Agent | Stack | Key Features |
| :---- | :---- | :----------- |
| **Java** | Spring Boot 4 + Java 21 | jOOQ, Flyway migrations, OpenAPI code generation, Gradle workflows |
| **Nuxt** | Nuxt 4 + Vue 3 + TypeScript | Orval API client, i18n, Vitest testing, TanStack Query |
| **EITS** | Security / Compliance | E-ITS compliance, process mapping, security class determination, audit logging |

### 💬 Commands (`commands/`)

Reusable prompt templates for common development tasks. Copy and paste into Cursor chat.

| Command | Purpose |
| :------ | :------ |
| `code-review.md` | Structured code review workflow with severity levels and fix prioritization |
| `deslop.md` | Remove AI-generated "slop" (unnecessary comments, defensive code, type bypasses) |

## Installation

### Option 1: Copy Rules to Your Project

Copy the rules you need into your project's `.cursor/rules/` directory:

```bash
# Copy all rules
cp -r rules/* your-project/.cursor/rules/

# Or copy specific categories
cp -r rules/common/* your-project/.cursor/rules/
cp -r rules/java-spring-boot/* your-project/.cursor/rules/
```

### Option 2: Copy Agent Configuration

For project-specific agent behavior, copy the appropriate `AGENTS.md` to your project root:

```bash
# For Spring Boot projects
cp agents/java/AGENTS.md your-project/AGENTS.md

# For Nuxt projects
cp agents/nuxt/AGENTS.md your-project/AGENTS.md

# For EITS compliance
cp agents/eits/AGENTS.md your-project/AGENTS.md
```

## How It Works

### Rules (`.mdc` files)

Rules are automatically applied by Cursor based on:

- **`globs`**: File patterns that trigger the rule (e.g., `**/*.java`)
- **`alwaysApply`**: Whether the rule applies to all files

Example rule header:

```yaml
---
description: Java standards (Java 21+) for code style, design, and language features
globs: **/*.java
alwaysApply: true
---
```

### Agents (`AGENTS.md`)

Agent files define:

- **Persona**: How the AI should behave
- **Commands**: Project-specific build/test commands
- **Boundaries**: What actions require approval
- **Checklists**: Step-by-step workflows for common tasks

## Customization

These configurations are starting points. Adapt them to your project:

1. **Modify rules** to match your team's conventions
2. **Update agent commands** to match your build tools
3. **Add project-specific boundaries** based on your architecture
4. **Create memory files** (`docs/agent-memory.md`) to track lessons learned

## Structure

```
cursor-prompts/
├── agents/
│   ├── eits/
│   │   └── AGENTS.md          # EITS Audit agent configuration
│   ├── java/
│   │   └── AGENTS.md          # Spring Boot agent configuration
│   └── nuxt/
│       └── AGENTS.md          # Nuxt/Vue agent configuration
├── commands/                  # Reusable prompt templates
│   ├── code-review.md
│   └── deslop.md
├── rules/
│   ├── common/                # Language-agnostic standards
│   │   ├── component-technical-standards.mdc
│   │   ├── integration-standards.mdc
│   │   └── security.mdc
│   ├── java-common/           # Java-specific standards
│   │   ├── application-logging.mdc
│   │   ├── audit-logging.mdc
│   │   ├── java-code-standards.mdc
│   │   └── jooq-database-access.mdc
│   └── java-spring-boot/      # Spring Boot standards
│       ├── spring-conventions.mdc
│       ├── spring-retry-conventions.mdc
│       └── spring-testing.mdc
├── LICENSE
└── README.md
```

## Contributing

Contributions welcome! When adding new rules or agents:

1. Follow the existing file format and structure
2. Include practical examples (valid and invalid)
3. Keep rules focused and actionable
4. Test with real projects before submitting

## License

[MIT](LICENSE) © 2025 E-government building blocks
