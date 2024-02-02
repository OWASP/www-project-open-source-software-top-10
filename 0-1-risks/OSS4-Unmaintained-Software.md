## Unmaintained software

**Description:**

A component or component version may not be actively developed or supported any more, i.e. patches for new functional and security bugs may not be developed.

Patch development may therefore need to be done by downstream developers with potentially less experience and knowledge regarding the affected component.

This can result in increased efforts and longer resolution times. During that time, system access or functionality may need to be restricted to avoid continued exposure.

**Examples:**

1. [core-js](https://www.theregister.com/2020/03/26/corejs_maintainer_jailed_code_release) (npm, 2020)
2. [Gorilla Web Toolkit](https://www.chainguard.dev/unchained/a-tale-of-two-software-security-risks) (Go, 2022)
3. [minimist](https://twitter.com/ljharb/status/1579610392414007299?lang=en) (npm, 2022)

**Actions:**

1. Check indicators for project liveliness and health.

    However, note that little activity can also be a sign of maturity. Projects that are considered feature-complete and mature will see less activity than projects under active development, and still receive timely patches in case of problems.

    Example indicators:

    - Recent issue and commit activity means the project is active.
    - A high ratio of issues opened by external contributors indicates that the project is active.
    - Activity from corporate affiliated accounts that indicate that the project can have reliable backing and support.
    - Activity from reputable accounts indicates that the repository is well-maintained.
    - The repository has frequent releases indicating a commitment to maintaining and supporting the codebase.


2. Search for information on a project's maintenance or support strategy, e.g., the presence and dates of long-term support (LTS) versions.

    The Spring project is a great example for documenting [support time frames](https://spring.io/projects/spring-boot#support).
3. Check the project page to see whether its has been archived, or whether there are any explicit statements regarding the project's maintenance status.

**References:**

1. OWASP Top 10 A06:2021 - Vulnerable and Outdated Components
2. [Bus factor](https://en.wikipedia.org/wiki/Bus_factor)
3. CWE-1104: Use of Unmaintained Third Party Components
4. CWE-1329: Reliance on Component That is Not Updateable
5. [Adoptoposs](https://github.com/adoptoposs/adoptoposs)
6. [Jazzband](https://jazzband.co/)