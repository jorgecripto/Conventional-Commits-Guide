# Conventional-Commits-Guide
Quick reference guide for the Conventional Commits specification.

# Conventional Commits Cheatsheet

The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history, which makes it easier to write automated tools on top of. This convention dovetails with Semantic Versioning (SemVer) by describing the features, fixes, and breaking changes made in commit messages.

## Structure

The commit message **MUST** be structured as follows:

<type>[optional scope]<!>: <description>
[optional body]
[optional footer(s)]

### Key Rules and Types

| Element | Description | SemVer Correlation | Example |
| :--- | :--- | :--- | :--- |
| **`type`** | The mandatory prefix (a noun) followed by the required terminal colon and space. | Determines the version bump. | `feat`, `fix`, `docs` |
| **`feat`** | A commit that introduces a **new feature** to the codebase. | Correlates with a **MINOR** release. | `feat(lang): add Polish language` |
| **`fix`** | A commit that **patches a bug** in the codebase. | Correlates with a **PATCH** release. | `fix: prevent racing of requests` |
| **`[optional scope]`** | A noun describing a section of the codebase surrounded by parentheses. | — | `feat(parser): add ability...` |
| **`BREAKING CHANGE`** | Introduces an incompatible API change. Indicated by a `BREAKING CHANGE:` footer or by adding `!` after the type/scope. | Correlates with a **MAJOR** release. | `feat!: send an email...` |
| **Other Types** | Types like `build`, `chore`, `ci`, `docs`, `style`, `refactor`, `perf`, and `test` are allowed. | No implicit effect on SemVer, unless they include a `BREAKING CHANGE`. | `docs: correct spelling of CHANGELOG` |

---

### Sources

This cheatsheet summarizes the key requirements and recommendations from the Conventional Commits Specification 1.0.0.

*   **Summary:** The specification defines an easy set of rules for creating an explicit, human- and machine-readable commit history that aligns with SemVer.
*   **Structure:** All commits **MUST** follow the format: `<type>[optional scope]: <description>`.
*   **SemVer Correlation:** The commit type dictates the resulting SemVer version bump: `feat` correlates with a MINOR release; `fix` correlates with a PATCH release; and any commit containing a `BREAKING CHANGE` correlates with a MAJOR release.
*   **Breaking Changes:** Breaking API changes **MUST** be indicated either by a footer starting with the uppercase text `BREAKING CHANGE:` or by appending an exclamation mark (`!`) immediately before the required colon in the header.
*   **Allowed Types:** Types other than `feat` and `fix` (such as `docs`, `chore`, `ci`, `refactor`, etc.) **MAY** be used.

---

