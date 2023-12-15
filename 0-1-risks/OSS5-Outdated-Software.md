## Outdated software

**Description:**

A project may use an old, outdated version of the component (though newer versions exist).

Falling too much behind the latest releases of a dependency can make it difficult to perform timely updates in emergency situations, e.g., when a vulnerability is disclosed for the version in use. Old releases may also not receive the same level of security assessment as recent versions, esp. whether they are affected by vulnerabilities. If a new version is syntactically or semantically incompatible with the current version in use, application developers may require significant update/migration efforts to resolve the incompatibility.

**Examples:**

1. [Spring Boot support time frames](https://spring.io/projects/spring-boot#support)

**Actions:**

1. Keep dependencies up-to-date, e.g., by using tools that create merge/pull requests with update suggestions, and making dependency updates recurring backlog items

**References:**

1. OWASP Top 10 A06:2021 – Vulnerable and Outdated Components.