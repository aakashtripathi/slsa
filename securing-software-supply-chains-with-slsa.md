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


