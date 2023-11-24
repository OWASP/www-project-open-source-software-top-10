## Immature-Software

**Description:**

An open source project may not apply development best-practices, e.g., not use a standard versioning scheme, have no regression test suite, no development or review guidelines or no documentation. As a result, a component may not work reliably or securely (in the sense of having security weaknesses that result in exploitable vulnerabilities).

The dependency on an immature component or project comes with operational risks. The dependent software may not work as expected and result in runtime reliability issues, or its use may be overly complex and expensive for the dependent software development organization.

For example, a component or project may lack documentation, may not use or comply with an established versioning scheme (which can result in breaking changes during component updates), or may not have a test suite to discover regressions introduced through pull/merge requests. Such cases can increase the effort of developers depending on such components.

**Examples:**

1. -

**Actions:**

1. Check whether a project follows development best-practices, e.g., the presence, quality and up-to-dateness of project documentation and release notes, the presence of badges to indicate test coverage or the presence of CI/CD pipelines to detect regressions.
2. A proxy for checking project maturity may also be the number of downstream dependents.

**References:**

1. OpenSSF Best Practices Badge Program
2. Common Weakness Enumeration
