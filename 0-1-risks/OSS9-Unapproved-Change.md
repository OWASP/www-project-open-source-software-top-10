## Unapproved Change (Mutable)

**Description:**

A component may change without developers being able to notice, review or approve such changes, e.g., because the download link points to an unversioned resource, because a versioned resource has been modified or tampered with or due to an insecure data transfer.

Using components that are not guaranteed to be identical when downloaded at different points in time are primarily a security risk. Attacks such as on the Codecov Bash Uploader demonstrate the risk of piping downloaded scripts directly to bash, without checking their integrity beforehand. Mutable components also threaten the stability and reproducibility of software builds.

**Examples:**

1. References to non-versioned shell scripts in CI/CD pipelines (e.g., https://codecov.io/bash)
2. References to Git repositories without commit identifier (e.g., https://raw.githubusercontent.com/…/main/install.sh)
3. HTTP links to package repositories (e.g., CVE-2021-26291)

**Actions:**

1. Use resource identifiers providing guarantees (or at least some degree of assurance) to always point to the same, immutable artifact.
2. Additionally, verify digests or signatures after component download and before installation/use
3. Use secure protocols for connection/distribution to avoid MITM attacks

**References:**

1. SLSA Immutable Reference
2. CWE-829: Inclusion of Functionality from Untrusted Control Sphere
3. CWE-830: Inclusion of Web Functionality from an Untrusted Source 
4. OWASP Top 10 A08:2021 – Software and Data Integrity Failures
5. Codecov Bash Uploader Security Update