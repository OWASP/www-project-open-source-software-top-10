## License and Regulatory Risk

**Description:**

A component or project may not have a license at all, one that is incompatible with the intended use by a downstream consumer, or one whose requirements are not or cannot be met by a downstream user.

A component may also violate license terms independent from downstream use, e.g., if it is licensed as GPL but includes files licensed under the original (4-clause) BSD license.

A component may also conflict with legal and regulatory requirements, e.g., related to FedRAMP certification or export control.

It is important to use components in compliance with their license terms. The absence of a license or non-compliant use can result in copyright or license infringements, which the copyright holder can take legal action against.

The violation of legal and regulatory requirements can constrain or hamper addressing certain verticals or markets.

**Examples:**

1. [Free Software Foundation, Inc. v. Cisco Systems, Inc.](https://www.fsf.org/licensing/complaint-2008-12-11.pdf) (2008)

**Actions:**

1. Identify acceptable licenses for the intended use of the component in the software under development.

    This should consider, for example, how the component is linked, the software's deployment model (cloud, on-premise/device) and the intended distribution scheme.
2. Comply with requirements stated in the open source licenses.
3. Avoid components without license.
4. Scrutinize component files for multiple and/or incompatible licenses.

**References:**

1. [OSI Approved Licenses](https://opensource.org/licenses/)
2. [SPDX License List](https://spdx.org/licenses/)
3. [REUSE](https://reuse.software/)
4. [Various Licenses and Comments about Them](https://www.gnu.org/licenses/license-list.en.html)
