## OSS-RISK-5 : Outdated software

**Description:**

A project may use an old, outdated version of the component (though newer versions exist).

Falling too much behind the latest releases of a dependency can make it difficult to perform timely updates in emergency situations, e.g., when a vulnerability is disclosed for the version in use. Old releases may also not receive the same level of security assessment as recent versions, esp. whether they are affected by vulnerabilities. If a new version is syntactically or semantically incompatible with the current version in use, application developers may require significant update/migration efforts to resolve the incompatibility.

**Examples:**

1. [Spring Boot support time frames](https://spring.io/projects/spring-boot#support)
2. Vulnerabilities affecting Apache Tomcat are ["not checked against the 8.0.x branch and will not be fixed"](https://tomcat.apache.org/security-8.html)

**Actions:**

1. Make dependency updates recurring backlog items
2. Automate the discovery and suggestion of updates, e.g. through merge/pull requests
3. Detect the introduction or breaking changes through change impact analysis tools

**References:**

1. OWASP Top 10:2021 [A06:2021 - Vulnerable and Outdated Components](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/)
2. Tools to check for the availability of new versions:
    - [Versions Maven Plugin](https://www.mojohaus.org/versions/versions-maven-plugin/index.html)
3. Tools to detect breacking changes:
    - [AexPy](https://github.com/StardustDL/aexpy)