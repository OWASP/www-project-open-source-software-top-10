## OSS-RISK-9 : Unapproved Change (Mutable)

**Description:**

A component may change without developers being able to notice, review or approve such changes, e.g., because the download link points to an unversioned resource, because a versioned resource has been modified or tampered with or due to an insecure data transfer.

Using components that are not guaranteed to be identical when downloaded at different points in time are primarily a security risk. Attacks such as on the Codecov Bash Uploader demonstrate the risk of piping downloaded scripts directly to bash, without checking their integrity beforehand. Mutable components also threaten the stability and reproducibility of software builds.

**Examples:**

1. References to non-versioned shell scripts in CI/CD pipelines
    -  [Codecov bash uploader](https://about.codecov.io/security-update/) (2021)
2. References to Git repositories without commit identifier
3. Insecure HTTP links to package registries
    - [CVE-2021-26291](https://nvd.nist.gov/vuln/detail/CVE-2021-26291) in Apache Maven (2022)

**Actions:**

1. Use resource identifiers providing guarantees (or at least some degree of assurance) to always point to the same, immutable artifact.
2. Verify digests or signatures after component download and before installation/use
3. Use secure protocols for connection/distribution to avoid MITM attacks

**References:**

1. SLSA [Immutable Reference](https://slsa.dev/spec/v0.1/requirements#immutable-reference)
2. [CWE-829: Inclusion of Functionality from Untrusted Control Sphere](https://cwe.mitre.org/data/definitions/829.html)
3. [CWE-830: Inclusion of Web Functionality from an Untrusted Source](https://cwe.mitre.org/data/definitions/830.html)
4. OWASP Top 10:2021 [A08:2021 - Software and Data Integrity Failures](https://owasp.org/Top10/A08_2021-Software_and_Data_Integrity_Failures/)