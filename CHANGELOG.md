# Changelog

All notable changes to this project will be documented in this file. Each pull request adds a fragment in `.changelog/`; the Release workflow folds them in here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 0.3.0 - 2026-11-12

### Changed

- Breaking: Require oxlint 1.0.0 or later ([#5])

### Removed

- Remove the `unicorn/no-for-loop` rule, which oxlint does not have: oxlint 1.x fails on unknown rules ([#5])

[#5]: https://github.com/studiometa/oxlint-config/pull/5

## 0.2.0 - 2026-02-13

### Added

- Add the `jsdoc` plugin, with the param, returns and property rules of `@studiometa/eslint-config` ([dc76bd3])
- Add the `vars-on-top` and `yoda` rules ([dc76bd3])

### Fixed

- Fix the publish workflow ([8252f19])

[dc76bd3]: https://github.com/studiometa/oxlint-config/commit/dc76bd3
[8252f19]: https://github.com/studiometa/oxlint-config/commit/8252f19

## 0.1.1 - 2026-02-13

### Removed

- Remove the `pedantic` category, because its `max-*` rules have impractical defaults ([7d9f716])

[7d9f716]: https://github.com/studiometa/oxlint-config/commit/7d9f716

## 0.1.0 - 2026-02-13

### Added

- Add the shared oxlint configuration, with the rules of `@studiometa/eslint-config` that oxlint supports ([17b02a4])

[17b02a4]: https://github.com/studiometa/oxlint-config/commit/17b02a4
