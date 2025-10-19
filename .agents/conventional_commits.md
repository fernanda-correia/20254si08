# Conventional Commits Configuration

## Commit Types

| Type | Description | Category |
|------|-------------|----------|
| `feat` | A new feature | Features |
| `fix` | A bug fix | Bug Fixes |
| `docs` | Documentation only changes | Documentation |
| `style` | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc) | Style |
| `refactor` | A code change that neither fixes a bug nor adds a feature | Refactoring |
| `perf` | A code change that improves performance | Performance |
| `test` | Adding missing tests or correcting existing tests | Testing |
| `build` | Changes that affect the build system or external dependencies | Build System |
| `ci` | Changes to our CI configuration files and scripts | Continuous Integration |
| `chore` | Other changes that don't modify src or test files | Chore |

## Format Structure

**Structure:** `<type>[optional scope]: <description>`

**Example:** `feat(auth): add login functionality`

## Rules

- All commit messages must follow the Conventional Commits specification
- Commit messages should be in the present tense
- First line should not exceed 72 characters
- Use imperative mood in the description
- Do not add periods at the end of the description
- Separate the subject from the body with a blank line if adding a body
- Can optionally add a scope in parentheses after the type
- Body should explain the 'what' and 'why' of the commit
- Footer can include breaking changes or issue references

## Valid Examples

- `feat: add user authentication`
- `fix: resolve memory leak in data processing`
- `docs: update API documentation`
- `refactor(auth): improve login validation`
- `feat(api)!: breaking change to API endpoints`
- `fix: correct typo in README`
- `test: add unit tests for user service`
- `build: update dependencies`

## Invalid Examples

- `Update files`
- `Fix bug`
- `Added new feature`
- `update README.md`
- `Improve performance of function`

## Scope Guidelines

- Scope should be a noun that describes the part of the system being changed
- Common scopes: auth, api, database, ui, config, etc.
- Use consistent naming for scopes across the project
- Scope is optional but recommended for clarity

## Breaking Changes

**Format:** A breaking change should include an exclamation mark (!) after the type/scope

**Example:** `feat(api)!: remove deprecated methods`

**Description:** Breaking changes should be clearly marked and explained in the commit body
