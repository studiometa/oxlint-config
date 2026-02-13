# @studiometa/oxlint-config

Shared [oxlint](https://oxc.rs/docs/guide/usage/linter) configuration for Studio Meta projects.

Mirrors the rules from [@studiometa/eslint-config](https://github.com/studiometa/eslint-config) where oxlint supports them. Use it as a fast complement or replacement for ESLint.

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

### Categories

| Category | Level | Description |
|----------|-------|-------------|
| `correctness` | error | Code that is outright wrong or useless |
| `suspicious` | warn | Code that is most likely wrong or useless |

### Plugins

- **unicorn** — Modern JavaScript best practices
- **jsdoc** — JSDoc comment validation

### Rules

**Best practices** (from `@studiometa/eslint-config`):
- `curly`: Require braces for all control statements
- `eqeqeq`: Require strict equality operators
- `no-alert`, `no-eval`: Disallow unsafe browser APIs
- `no-empty-function`: Disallow empty function bodies
- `no-var`: Require `let` or `const`
- `vars-on-top`: Require variable declarations at the top of scope
- `yoda`: Disallow Yoda conditions

**JSDoc** (matching `eslint-plugin-jsdoc` rules):
- `require-param`, `require-param-name`, `require-param-type`
- `require-returns`, `require-returns-type`
- `require-property`, `require-property-name`, `require-property-type`
- `check-property-names`, `check-tag-names`

**Unicorn** (matching `eslint-plugin-unicorn` rules):
- Prefer modern DOM APIs (`querySelector`, `append`, `remove`, etc.)
- Prefer modern array methods (`find`, `flat`, `flatMap`, `some`, `includes`)
- Prefer modern string methods (`replaceAll`, `slice`, `startsWith`, `endsWith`)
- Disallow common anti-patterns (`instanceof Array`, `document.cookie`, etc.)

### Rules not available in oxlint

The following `@studiometa/eslint-config` rules have no oxlint equivalent and require ESLint:

- `dot-notation`, `no-implicit-coercion`, `no-implicit-globals`, `no-multi-spaces`
- `no-param-reassign`, `no-useless-return`, `object-shorthand`
- `prefer-const`, `prefer-template`, `strict`, `wrap-iife`
- `unicorn/no-array-push-push`, `unicorn/prefer-at`, `unicorn/prefer-default-parameters`
- `unicorn/prefer-keyboard-event-key`
- Most `jsdoc/*` formatting rules (`check-alignment`, `multiline-blocks`, `no-multi-asterisks`, etc.)

See [oxlintrc.json](./oxlintrc.json) for the complete rule list.

## License

MIT © [Studio Meta](https://www.studiometa.fr)
