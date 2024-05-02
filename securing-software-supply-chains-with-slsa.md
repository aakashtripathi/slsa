# Securing Software Supply Chains with SLSA 

The cybersecurity landscape has been rattled by a spate of supply chain attacks such as the SolarWinds and Codecov attacks. These breaches not only underscore the vulnerability of software supply chains but also highlight the urgent need for robust security measures to safeguard against such threats. With adversaries increasingly targeting the software development process itself, the imperative for ensuring the integrity and trustworthiness of every component within the supply chain has never been more apparent.

## Enter SLSA

Supply-chain Levels for Software Artifacts, or SLSA ("salsa") is a security framework, a checklist of standards and controls to prevent tampering, improve integrity, and secure packages and infrastructure. When implemented in conjunction with automated testing tools in the DevSecOps pipeline, secure coding practices, and strong third-party software vetting, SLSA can be an important part of a comprehensive software supply chain security strategy.

## Understanding SLSA

SBOM or "Software Bill of Materials" is often reffered to as the **ingredient label** of software, extending the same analogy SLSA can be thought of as all the safety guidelines that make an ingredient list credible.

The SLSA framework offers a trusted system with clear guidelines and tamper-proof evidence at every stage of software development. This ensures not only that no unexpected changes are made to the software, but also that the software's "ingredients" are accurately represented and haven't been altered. Essentially, SLSA safeguards against:

- Unauthorized modifications to the code by applying a tamper-evident "seal" to the code post source control.
- Ensuring that uploaded artifacts were indeed built by the expected CI/CD platform, indicated by a distinct "stamp" showing the build platform's origin.
- Mitigating threats to the build platform itself by implementing best practices for build platform services.

## Threats To The Software Supply Chain



SLSA primarily focuses on maintaining the integrity of the software supply chain, with a secondary emphasis on ensuring availability. Integrity entails protecting against unauthorized modifications or tampering throughout the software lifecycle. Under SLSA, integrity is further categorized into source integrity and build integrity.

- Source integrity involves verifying that all alterations to the source code align with the intentions of the software producer. As defining an organization's intent can be complex, SLSA approximates this by requiring approval from two authorized representatives.
- Build integrity ensures that the package is constructed from the correct, unaltered sources and dependencies as per the software producer's build recipe. Additionally, it ensures that artifacts remain unmodified as they transition through various development stages.
- Availability ensures that the package remains buildable and maintainable in the future, and that all code and change history are accessible for investigations and incident response.
