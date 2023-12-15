## Under/over-sized Dependency

**Description:**

A component may provide very little functionality (e.g. npm micro packages) or a lot of functionality (of which only a fraction may be used).

Very small components, e.g. ones containing few lines of code only, are subject to the same supply chain risks as large ones, e.g. account take-over, malicious pull requests or CI/CD vulnerabilities, for comparably little functionality. In other words, in exchange for very few lines of code used, the consumer’s security becomes dependent on the upstream project’s security and development posture.
 
Very large components, on the other hand, may have accumulated many features that are not needed in standard use-cases, but contribute to the component’s attack surface. Additionally, such unused features may also bring in additional, unused dependencies (bloated dependencies).

**Examples:**

1. Apache Log4j (a large dependency coming with many features)
2. Left-pad (a small dependency)

**Actions:**

1. Redevelop the specific functionality needed internally.

**References:**

1. Feature creep
2. [A comprehensive study of bloated dependencies in the Maven ecosystem](https://link.springer.com/article/10.1007/s10664-020-09914-8#:~:text=Bloated%20dependencies%20are%20libraries%20that,binary%20and%20increase%20maintenance%20effort)
