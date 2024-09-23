## OSS-RISK-10 : Under/over-sized Dependency

**Description:**

A component may provide very little functionality (e.g. npm micro packages) or a lot of functionality (of which only a fraction may be used).

Very small components, e.g. ones containing few lines of code only, are subject to the same supply chain risks as large ones, e.g. account take-over, malicious pull requests or CI/CD vulnerabilities, for comparably little functionality. In other words, in exchange for very few lines of code used, the consumer's security becomes dependent on the upstream project's security and development posture.
 
Very large components, on the other hand, may have accumulated many features that are not needed in standard use-cases, but contribute to the component's attack surface. Additionally, such unused features may also bring in additional, unused dependencies (bloated dependencies).

**Examples:**

1. [Apache Log4j](https://logging.apache.org/log4j/2.x/)

    Included functionality to download and execute arbitrary Java classes from remote servers, which eventually led to [Log4Shell](https://en.wikipedia.org/wiki/Log4Shell).  

2. [Left-pad](https://www.theregister.com/2016/03/23/npm_left_pad_chaos/) (npm, 2016)

    Contained 11 lines of code to pad strings. Its removal from npm broke the builds of numerous downstream consumers.

**Actions:**

1. Become aware of unused component capabilities, esp. if they use critical (security sensitive) APIs such as to establish network connections.

    Evaluate possibilities to disable unused capabilities, or move to smaller alternative open source components with fewer capabilities.
2. Become aware of micro packages, and consider redeveloping their functionality internally.

**References:**

1. Definition: [Feature creep](https://en.wikipedia.org/wiki/Feature_creep)
2. Tools to uncover the use of security sensitive APIs:
    - Google [Capslock](https://github.com/google/capslock) for Go
    - Microsoft [Application Inspector](https://github.com/microsoft/ApplicationInspector) for various programming languages
    - Rahman et al.: [Less Is More](https://arxiv.org/pdf/2408.02846): A Mixed-Methods Study on Security-Sensitive API Calls in Java for Better Dependency Selection
