## OSS-RISK-2 : Compromise of Legitimate Package

**Description:**

Attackers may compromise resources that are part of an existing legitimate project or of the distribution infrastructure in order to inject malicious code into a component, e.g, through hijacking the accounts of legitimate project maintainers or exploiting vulnerabilities in package repositories.

Malicious code can be executed on end-user systems or on systems belonging to the organization that develops and/or operates the dependent software (e.g., build systems or developer workstations). The confidentiality, integrity and availability of systems and the data processed/stored thereon is at risk.

**Examples:**

1. [Event-stream](https://blog.npmjs.org/post/180565383195/details-about-the-event-stream-incident): This attack on a legitimate component targeted users of Copay Bitcoin wallets.
2. [The SolarWinds Cyber-Attack](https://www.cisecurity.org/solarwinds)

**Actions:**

There's no single action to detect and prevent the ingestion of compromised packages. Organizations should consult emerging standards and frameworks like the Secure Supply Chain Consumption Framework (S2C2F) to inform themselves about possible safeguards, which should be selected and prioritized according to individual security requirements and risk appetite.

Example actions comprise:
1. Verify component provenance according to SLSA
2. Build component from the sources (yourself or a trusted 3rd-party)
3. Review code manually and/or automatically
4. Retrieve all components from a secured internal store (such binary repositories host home-made binaries and mirror external components)

**References:**

1. [Secure Supply Chain Consumption Framework](https://www.microsoft.com/en-us/securityengineering/opensource) (S2C2F)
2. [Risk Explorer for Software Supply Chains](https://riskexplorer.endorlabs.com/) Subvert Legitimate Package (AV-001)
3. [Supply chain Levels for Software Artifacts](https://slsa.dev/) (SLSA)
4. MITRE ATT&CK [T1195.001 Compromise Software Dependencies and Development Tools](https://attack.mitre.org/techniques/T1195/001/)
5. OWASP Top 10 CI-CD Security Risks [CICD-SEC-3: Dependency Chain Abuse](https://owasp.org/www-project-top-10-ci-cd-security-risks/CICD-SEC-03-Dependency-Chain-Abuse)
6. OWASP Software Component Versification Standard (SCVS) [V6 Pedigree and Provenance](https://owasp-scvs.gitbook.io/scvs/v6-pedigree-and-provenance)