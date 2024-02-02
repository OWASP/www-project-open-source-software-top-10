## Name Confusion Attacks

**Description:**

Attackers may create components whose names ressemble names of legitimate open-source or system components (typo-squatting), suggest trustworthy authors (brand-jacking) or play with common naming patterns in different languages or ecosystems.

Malicious code can be executed on end-user systems or on systems belonging to the organization that develops and/or operates the dependent software (e.g., build systems or developer workstations). The confidentiality, integrity and availability of systems and the data processed/stored thereon is at risk.

**Examples:**

1. [Colourama](https://bertusk.medium.com/cryptocurrency-clipboard-hijacker-discovered-in-pypi-repository-b66b8a534a8) (PyPI, 2018): Typo-squatting attack on the legitimate Python package "colorama", redirecting Bitcoin transfers to an attacker-controlled wallet.

**Actions:**

Prior to installing/using a component: 
1. Check code characteristics (pre/post installation hooks, encoded payloads, etc.) and project characteristics (source code repository, maintainer accounts, release frequency, number of downstream users, etc.) for leading risk indicators. Note that some component metadata is not verified by package repositories, thus, can easily be forged by attackers.
2. Verify signatures (if any)

**References:**

1. Secure Supply Chain Consumption Framework (S2C2F)
2. Risk Explorer for Software Supply Chains - Create Name Confusion with Legitimate Package (AV-200)
3. OpenSSF Supply chain Levels for Software Artifacts (SLSA)
4. MITRE ATT&CK Compromise Software Dependencies and Development Tools