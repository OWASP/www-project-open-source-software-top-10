## Untracked Dependencies

**Description:**

Project developers may not be aware of a dependency on a component at all, e.g., because it is not part of an upstream component's SBOM, because SCA tools are not run or do not detect it, or because the dependency is not established using a package manager.

Flying under the radar, the respective component cannot be checked or monitored for any of the other deficiencies.

**Examples:**

1. Incomplete SBOMs received for upstream components or produced by SCA tools
2. Inclusion of 3rd-party code in a managed (tracked) dependency, e.g.
    - code snippets
    - source code files (copied as-is into the dependency's sources, also called "vendored")
    - compiled code (e.g., platform-specific binaries or Java archives/class files, also called rebundling)
3. Dependencies not established through the manifest files of package managers like PIP or Maven, e.g. manual or scripted installation through brew or apt-get 
4. IDE plugins, build scripts, test dependencies or other developer tools, though not included in the dependent software itself, still pose security and operational risks

**Actions:**

1. Evaluate and compare SCA tools regarding their capability to produce accurate bills of materials, both at coarse-granular level (e.g., dependencies declared with help of package management tools likes Maven or npm) and fine-granular level (e.g., artifacts like single files included "out of band", i.e., without using package managers).

**References:**

1. OWASP Software Component Versification Standard (SCVS) [V1 Inventory and V2 Software Bills of Materials](https://owasp-scvs.gitbook.io/scvs/v1-inventory)
2. Research on rebundling
    - Seth Larson: [Patching the libwebp vulnerability across the Python ecosystem](https://sethmlarson.dev/security-developer-in-residence-weekly-report-16) (2023)
    - J Rack, et al.: [Jack-in-the-box: An Empirical Study of JavaScript Bundling on the Web and its Security Implications](https://publications.cispa.saarland/4036/1/Bundlers_Study_Submission-camera-ready.pdf) (2023)
    - A Dann, et al.: [Identifying Challenges for OSS Vulnerability Scanners - A Study & Test Suite](https://www.bodden.de/pubs/dph+21identifying.pdf) (2021)
3. Anand Sawant: [Dependency Resolution in Python: Beware The Phantom Dependency](https://www.endorlabs.com/learn/dependency-resolution-in-python-beware-the-phantom-dependency) (2023)