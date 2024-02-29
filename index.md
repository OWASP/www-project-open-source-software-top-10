---

layout: col-sidebar
title: OWASP Open Source Software Top 10
tags: example-tag
level: 2
type: 
pitch: A very brief, one-line description of your project

---

![top 10 oss risks](https://uploads-ssl.webflow.com/656eaf5c6da3527caf362363/65cc002b9f2f0a2f881be5ee_owasp.png)

Despite the heavy reliance on OSS in the software supply chain, the industry lacks a consistent way to understand and measure risk for OSS. Risk management in OSS started with license management, and then evolved to CVEs, but we still lack a holistic approach to OSS risk management that encompasses security, legal, and opertional aspects. With this document, we're excited to collaborate with industry experts and leaders to create just that. 

Over the last decade of reliance on OSS, known vulnerabilities, captured as CVEs, have emerged as the key metric of security. Known vulnerabilities, while an important signal, typically capture mistakes made by well-intentioned developers. These mistakes could be exploited by attackers and should be fixed, but they hardly encompass the full spectrum of risks that a reliance on OSS includes. 

Operational risks, like ones introduced by outdated or unmaintained software, or next-generation supply chain attacks like name confusion attacks, cannot be captured by CVEs. These risks are significant, as highlighted by the recent [Open Source Security and Risk Analysis report](https://www.synopsys.com/content/dam/synopsys/sig-assets/reports/rep-ossra-2023.pdf) by Synopsys:

- 89% of codebases contain OSS that is more than 4 years out of date
- 91% of codebases contain components that have had no new development in over two years

On [The State of Dependency Management](https://endorlabs.webflow.io/learn/state-of-dependency-management), the Station 9 research team from Endor Labs uncovered that 95% of vulnerabilities exist in transitive dependencies (the software packages automatically brought in by the OSS selected by developers). And out of those, many are not actually reachable, or will cause a devastating ripple effect of incompatibility if they were updated. With this list, which was peer-reviewed and contributed to by over 20 CISOs and CTOs, the team sought to find the top risks security and development teams should be ready for, both operational and security. 

The top 10 OSS risks are:

| Risk    | Description | something |
| -------- | ------- |---|
| [OSS-RISK-1 Known Vulnerabilities](./0-1-risks/OSS1-Known-Vulnerabilities.md)	  | A component version may contain vulnerable code, accidentally introduced by its developers. Vulnerability details are publicly disclosed, e.g, through CVE, GitHub Security Advisories or other, more informal communication channels. Exploits and patches may or may not be available.	    |Security|
| [OSS-RISK-2 Compromise of Legitimate Package](./0-1-risks/OSS2-Compromise-Legitimate-Package.md)	 | Attackers may compromise resources that are part of an existing legitimate project or of the distribution infrastructure in order to inject malicious code into a component, e.g, through hijacking the accounts of legitimate project maintainers or exploiting vulnerabilities in package repositories.	     |Security|
| [OSS-RISK-3 Name Confusion Attacks](./0-1-risks/OSS3-Name-Confusion-Attack.md)	    | Attackers may create components whose names resemble names of legitimate open-source or system components (typo-squatting), suggest trustworthy authors (brand-jacking) or play with common naming patterns in different languages or ecosystems (combo-squatting).	    |Security|
| [OSS-RISK-4 Unmaintained Software](./0-1-risks/OSS4-Unmaintained-Software.md)	    | A component or component version may not be actively developed any more, thus, patches for functional and non-functional bugs may not be provided in a timely fashion (or not at all) by the original open source project.	    |Ops|
| [OSS-RISK-5 Outdated Software](./0-1-risks/OSS5-Outdated-Software.md)	    | A project may use an old, outdated version of the component (though newer versions exist).	    |Ops|
| [OSS-RISK-6 Untracked Dependencies](./0-1-risks/OSS6-Untracked-Dependencies.md)	    | Project developers may not be aware of a dependency on a component at all, e.g., because it is not part of an upstream component's SBOM, because SCA tools are not run or do not detect it, or because the dependency is not established using a package manager.	    |Security, Ops|
| [OSS-RISK-7 License Risk](./0-1-risks/OSS7-License-Regulatory-Risks.md)		    | A component or project may not have a license at all, or one that is incompatible with the intended use or whose requirements are not or cannot be met.	    |Ops|
| [OSS-RISK-8 Immature Software](./0-1-risks/OSS8-Immature-Software.md)		    | An open source project may not apply development best-practices, e.g., not use a standard versioning scheme, have no regression test suite, review guidelines or documentation. As a result, a component may not work reliably or securely.	    |Ops|
| [OSS-RISK-9 Unapproved Change](./0-1-risks/OSS9-Unapproved-Change.md) | A component may change without developers being able to notice, review or approve such changes, e.g., because the download link points to an unversioned resource, because a versioned resource has been modified or tampered with or due to an insecure data transfer.	    |Security, Ops|
| [OSS-RISK-10 Under/over-sized Dependency](./0-1-risks/OSS10-UnderOversized-Dependency.md)		    | A component may provide very little functionality (e.g. npm micro packages) or a lot of functionality (of which only a fraction may be used).	    |Security, Ops|

## Authors and Contributors
![Authors](https://assets-global.website-files.com/6574c9e538a34feac8cec013/65bead00803e405540ee1711_63fe9397e0e9522788307ec1_Screenshot%25202023-02-28%2520at%25203.51.37%2520PM.png)

## Dependency Management 101
To better understand how these risks may affect us, let us quickly review some basic concepts of dependency management using a simple example. Just skip this section if you’re familiar with dependency management.

The root node of the dependency graph displayed below represents the example project. The child nodes of the root represent 9 open source components the project “directly” depends on. Those components, however, depend on other components as well, all of which become “transitive” or “indirect” dependencies from the perspective of the top-level project.

Direct dependencies are consciously selected by the project developers, e.g., through the declaration in a manifest file such as package.json (Node.js/npm) or pom.xml (Java/Maven) file. Package managers take care of downloading and installing those direct dependencies from 3rd party package repositories to the developers workstation or a CI/CD system. When doing so, package managers also identify transitive dependencies, resolve potential version conflicts and install them locally. In other words, plenty of components are downloaded in an automated fashion in order to make sure all code required by the example project (and more) is present on the developer machine.
![dependency management](https://assets-global.website-files.com/6574c9e538a34feac8cec013/65bead00803e405540ee171b_63fe92d1c33d5b05cc2c6230_LzJxmbByCB9JLF_BXzxj_p8m2CnDZe0Xkk07Q06KTyV2zgaCdIaNc6AkU7gd8klHAJykYTcDAU8xDnRh7lBUtBQ0eVBGDV_dPyC_lK8fzOUdq33GtEI7NA9B_Q0-Xhw8MgocdVsyuuB9z7WiWv3_Mok.png)
This high degree of automation boosted the reuse of open source components in today’s software development. As a result, large portions of modern software have not been specifically developed for an application at hand, but come from generic open source projects. Looking again at the dependency graph, it is not surprising that the ratio of code written for the project itself (the root node) to the code of open source components is 1:4 or less. And we haven’t even touched upon IDEs, build tools etc.
