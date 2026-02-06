# Issue #3: Complete repo quality standardization

Link: [Issue #3](https://github.com/AFixt/wcag-as-json/issues/3)

## Context

PR #4 implemented the bulk of issue #3 requirements. This follow-up completes the remaining items.

## What PR #4 already did

- Dependabot config (.github/dependabot.yml)
- CI workflow (.github/workflows/ci.yml) - validate JSON, prettier check, markdownlint
- Security workflow (.github/workflows/security.yml) - npm audit, CodeQL, OWASP, license check
- Prettier config (.prettierrc, .prettierignore)
- Markdownlint config (.markdownlint.json)
- package.json scripts: format, format:check, lint:md, security:audit, security:check
- .gitignore updated
- Fixed validate:schema script bug

## Remaining work

1. **Fix markdown lint errors** - CLAUDE.md and README.md have lint issues
2. **Add Husky + lint-staged** - Pre-commit hooks (recommended in issue)
3. **Verify all checks pass cleanly**

## Items correctly skipped (not applicable)

- ESLint: No JS/TS source code
- Stylelint: No CSS files
- jscpd: No source code to detect duplication in
