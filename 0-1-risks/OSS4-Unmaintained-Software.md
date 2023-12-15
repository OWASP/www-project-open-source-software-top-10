## Unmaintained software

**Description:**

A component or component version may not be actively developed any more, thus, patches for functional and security bugs may not be available.

The patch development may need to be done by downstream developers with potentially less experience and knowledge regarding the affected component. This can result in increased efforts and longer resolution times. During that time, the system remains exposed.

**Examples:**

1. Gorilla Web Toolkit
2. Adoptoposs or Jazzband (Web pages used by projects to find new co-maintainers)
3. Spring Boot support time frames
4. https://www.theregister.com/2020/03/26/corejs_maintainer_jailed_code_release

**Actions:**

1. Check project liveliness and health, e.g., the number of active maintainers/contributors, release frequency or the number of issues and pull requests opened/closed. Note, however, that little activity can also be a sign of maturity. Projects that are considered feature-complete and mature will see less activity than projects under active development, and still receive timely patches in case of problems.
2. Search for information on a project’s maintenance or support strategy, e.g., the presence and dates of LTS versions
3. Check the project page for explicit mentions of maintenance status (e.g., an archived GitHub project)

**References:**

1. OWASP Top 10 A06:2021 – Vulnerable and Outdated Components
2. Bus factor
3. CWE-1104: Use of Unmaintained Third Party Components
4. CWE-1329: Reliance on Component That is Not Updateable
