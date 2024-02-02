## Under/over-sized Dependency

**Description:**

A component may provide very little functionality (e.g. npm micro packages) or a lot of functionality (of which only a fraction may be used).

Very small components, e.g. ones containing few lines of code only, are subject to the same supply chain risks as large ones, e.g. account take-over, malicious pull requests or CI/CD vulnerabilities, for comparably little functionality. In other words, in exchange for very few lines of code used, the consumer's security becomes dependent on the upstream project's security and development posture.
 
Very large components, on the other hand, may have accumulated many features that are not needed in standard use-cases, but contribute to the component's attack surface. Additionally, such unused features may also bring in additional, unused dependencies (bloated dependencies).

**Examples:**

1. [Apache Log4j](https://logging.apache.org/log4j/2.x/)

    Included functionality to download and execute arbitrary Java class from remote servers, which eventually led to [Log4Shell](https://en.wikipedia.org/wiki/Log4Shell).  

2. [Left-pad](https://www.theregister.com/2016/03/23/npm_left_pad_chaos/) (npm, 2016)

    Contained 11 lines of code to pad strings. Its removal from npm broke the builds of numerous downstream consumers.

**Actions:**

1. Become aware of unused component capabilities, esp. if they use critical APIs such as to establish network connections.

    Evaluate possibilities to disable unused capabilities, or move to smaller alternative open source components with fewer capabilities.
2. Become aware of micro packages, and consider redeveloping their functionality internally.

**References:**

1. Definition: [Feature creep](https://en.wikipedia.org/wiki/Feature_creep)
2. [Capslock: What is your code really capable of?](https://security.googleblog.com/2023/09/capslock-what-is-your-code-really.html) (Go, 2023)
2. C. Soto-Valero et al.: [A comprehensive study of bloated dependencies in the Maven ecosystem](https://link.springer.com/article/10.1007/s10664-020-09914-8#:~:text=Bloated%20dependencies%20are%20libraries%20that,binary%20and%20increase%20maintenance%20effort) (EMSE, 2021)
