## Known vulnerabilities in dependencies

**Description:**

A component version may contain vulnerable code, accidentally introduced by its developers. Vulnerability details are publicly disclosed, e.g, through a CVE. Exploits and patches may or may not be available.

The vulnerability may be exploitable in the context of the downstream software, which could compromise the confidentiality, integrity or availability of the respective system or its data.

**Examples:**

1. Example 1: CVE-2017-5638 in Apache Struts (which caused the Equifax data breach)
2. Example 2: CVE-2021-44228 in Apache Log4j (Log4Shell)

**Actions:**

1. Regularly scan for vulnerabilities in all OSS versions used.
2. Prioritize findings to optimize resource allocation, e.g., by using SAST tools to determine whether vulnerable code can be executed in the context of the dependent software.

**References:**

1. OWASP Top 10:2021 [A06:2021 - Vulnerable and Outdated Components](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/)
