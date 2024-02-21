## Known vulnerabilities in dependencies

**Description:**

A component version may contain vulnerable code, accidentally introduced by its developers. Vulnerability details are publicly disclosed, e.g, through CVE, GitHub Security Advisories or other, more informal communication channels. Exploits and patches may or may not be available.

The vulnerability may be exploitable in the context of the downstream software, which could compromise the confidentiality, integrity or availability of the respective system or its data, allow laterial movements in the target environment or have other negative effects.

**Examples:**

1. [CVE-2017-5638](https://cwiki.apache.org/confluence/display/WW/S2-045) in Apache Struts, which caused the [Equifax data breach](https://en.wikipedia.org/wiki/2017_Equifax_data_breach)
2. [CVE-2021-44228](https://logging.apache.org/log4j/2.x/security.html#CVE-2021-44228) in Apache Log4j, also called [Log4Shell](https://en.wikipedia.org/wiki/Log4Shell)

**Actions:**

1. Monitor applications, containers and systems for the presence of (direct and transitive) open source dependencies with known vulnerabilities
2. Prioritize the analysis and mitigation on the basis of, for instance
    - Scores and metrics like [CVSS](https://www.first.org/cvss/) and [EPSS](https://www.first.org/epss/)
    - Threat intelligence like the availability and maturity of exploit code, or information on attacks observed in the wild such as provided by the CISA [KEV catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
    - DAST and SAST tools, which determine if vulnerable code can be executed in the context of the dependent software

**References:**

1. OWASP Top 10:2021 [A06:2021 - Vulnerable and Outdated Components](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/)
