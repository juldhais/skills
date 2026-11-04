# Code standard

## Scope
- In scope: {{folders the agent may change}}. Ignore {{others}} unless asked.

## Structure
```
{{one line per top-level folder/project: role and stack}}
```

## Rules
- {{Source of truth; what must not change to simplify another layer}}
- {{Security/authorization model}}
- {{Naming: identifiers vs UI text}}

## Conventions
- **Naming**: {{per language}}
- **Comments**: only for non-obvious why.

## Validation
- Build: {{command}}
- Lint/test: {{commands and folder}}

## Security
- Never commit secrets, tokens or connection strings. {{Where local config lives.}}
