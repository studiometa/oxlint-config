# @studiometa/oxlint-config

Shared [oxlint](https://oxc.rs/docs/guide/usage/linter) configuration for Studio Meta projects.

## Installation

```bash
npm install -D @studiometa/oxlint-config oxlint
```

## Usage

Create an `oxlintrc.json` file at the root of your project:

```json
{
  "extends": ["./node_modules/@studiometa/oxlint-config/oxlintrc.json"]
}
```

Then run oxlint:

```bash
npx oxlint
```

### Override rules

Add or override rules in your project config:

```json
{
  "extends": ["./node_modules/@studiometa/oxlint-config/oxlintrc.json"],
  "rules": {
    "no-console": "off"
  }
}
```

## What's included

This config enables:

- **Correctness** rules as errors (oxlint default category)
- **Suspicious** and **Pedantic** rules as warnings
- **Unicorn** plugin for modern JavaScript best practices

### Rule overview

| Category | Level | Description |
|----------|-------|-------------|
| `correctness` | error | Code that is outright wrong or useless |
| `suspicious` | warn | Code that is most likely wrong or useless |
| `pedantic` | warn | Lints which are rather strict or have occasional false positives |

### Key rules

**Best practices:**
- `curly`: Require braces for all control statements
- `eqeqeq`: Require strict equality operators
- `no-alert`, `no-eval`: Disallow unsafe browser APIs
- `no-empty-function`: Disallow empty function bodies
- `no-var`: Require `let` or `const`

**Unicorn (modern JS):**
- Prefer modern DOM APIs (`querySelector`, `append`, `remove`, etc.)
- Prefer modern array methods (`find`, `flat`, `flatMap`, `some`, `includes`)
- Prefer modern string methods (`replaceAll`, `slice`, `startsWith`, `endsWith`)
- Disallow common anti-patterns (`instanceof Array`, `document.cookie`, etc.)

See [oxlintrc.json](./oxlintrc.json) for the complete rule list.

## Compatibility

This config mirrors the rules from [@studiometa/eslint-config](https://github.com/studiometa/eslint-config) where oxlint supports them. Use it as a fast complement or replacement for ESLint in projects where speed matters.

## License

MIT © [Studio Meta](https://www.studiometa.fr)
