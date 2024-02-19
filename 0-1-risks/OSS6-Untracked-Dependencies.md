## Untracked Dependencies

**Description:**

Project developers may not be aware of a dependency on a component at all, e.g., because it is not part of an upstream component's SBOM, because SCA tools are not run or do not detect it, or because the dependency is not established using a package manager.

Flying under the radar, the respective component cannot be checked or monitored for any of the other deficiencies.

**Examples:**

1. Incomplete SBOMs received for upstream components or produced by SCA tools
2. Inclusion of 3rd-party code in a managed (tracked) dependency, e.g., code snippets, 3rd-party source code files (copied as-is into the dependency's sources) or 3rd-party compiled code (e.g., platform-specific binaries or re-bundled Java archives/class files)
3. Not using a package manager at all
4. IDE plugins, build scripts, test dependencies or other developer tools, though not included in the dependent software itself, still pose security and operational risks.

**Actions:**

1. Evaluate and compare SCA tools regarding their capability to produce accurate bills of materials, both at coarse-granular level (e.g., dependencies declared with help of package management tools likes Maven or npm) and fine-granular level (e.g., artifacts like single files included "out of band", i.e., without using package managers) 

**References:**

1. OWASP Software Component Versification Standard (SCVS) [V1 Inventory and V2 Software Bills of Materials](https://owasp-scvs.gitbook.io/scvs/v1-inventory)
