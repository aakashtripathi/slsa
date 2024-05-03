# Securing Software Supply Chains with SLSA 

![image](https://github.com/aakashtripathi/slsa/assets/67234531/b2c2ebae-cef6-4048-a9dd-226325e3d107)


The cybersecurity landscape has been rattled by a spate of supply chain attacks . These breaches not only underscore the vulnerability of software supply chains but also highlight the urgent need for robust security measures to safeguard against such threats. With adversaries increasingly targeting the software development process itself, the imperative for ensuring the integrity and trustworthiness of every component within the supply chain has never been more apparent.

In a series of articles, we will explore Supply-chain Levels for Software Artifacts, or SLSA ("salsa") which is a security framework, a checklist of standards and controls to prevent tampering, improve integrity, and secure packages and infrastructure. When implemented in conjunction with automated testing tools in the DevSecOps pipeline, secure coding practices, and strong third-party software vetting, SLSA can be an important part of a comprehensive software supply chain security strategy.

## Understanding SLSA

Google's security team unveiled SLSA in June 2021, drawing inspiration from their long-standing practice of "Binary Authorization for Borg," which has safeguarded the company's production workloads for nearly a decade. The release of SLSA coincided with a tumultuous period in software supply chain security, following the disclosure of exploits such as SolarWinds and the Codecov bash uploader vulnerabilities. The blog read :

*"The goal of SLSA is to improve the state of the industry, particularly open source, to defend against the most pressing integrity threats. With SLSA, consumers can make informed choices about the security posture of the software they consume."*

The SLSA framework offers a trusted system with clear guidelines and tamper-proof evidence at every stage of software development.SBOM or "Software Bill of Materials" is often referred to as the ingredient label of software, extending the same analogy SLSA can be thought of as all the safety guidelines that make an ingredient list credible.

This ensures not only that no unexpected changes are made to the software, but also that the software's "ingredients" are accurately represented and haven't been altered. Essentially, SLSA safeguards against:

- Unauthorized modifications to the code by applying a tamper-evident "seal" to the code post source control.
- Ensuring that uploaded artifacts were indeed built by the expected CI/CD platform, indicated by a distinct "stamp" showing the build platform's origin.
- Mitigating threats to the build platform itself by implementing best practices for building platform services.

---

## Threats To The Software Supply Chain

Prior to SLSA, there were only isolated solutions capable of detecting and addressing specific vulnerabilities at different stages of the supply chain. Unlike these fragmented approaches, SLSA offers a holistic framework designed to safeguard the entire software supply chain. It not only outlines strategies to mitigate threats across all supply chain components but also furnishes security assurances that fortify against attacks in a dynamic security landscape.

![Threats To The Software Supply Chain](/images/Source.png)

SLSA primarily focuses on maintaining the integrity of the software supply chain, with a secondary emphasis on ensuring availability. Integrity entails protecting against unauthorized modifications or tampering throughout the software lifecycle. Under SLSA, integrity is further categorized into source integrity and build integrity.

- Source integrity involves verifying that all alterations to the source code align with the intentions of the software producer. As defining an organization's intent can be complex, SLSA approximates this by requiring approval from two authorized representatives.
- Build integrity ensures that the package is constructed from the correct, unaltered sources and dependencies as per the software producer's build recipe. Additionally, it ensures that artifacts remain unmodified as they transition through various development stages.
- Availability ensures that the package remains buildable and maintainable in the future and that all code and change history are accessible for investigations and incident response.

---

## Tracks & Levels 

SLSA is spoken of in terms of *tracks* & *levels*. In a SLSA framework, each track concentrates on a specific facet of the software supply chain, such as the Build Track. While SLSA v1.0 encompasses solely the Build Track, forthcoming iterations will introduce additional tracks addressing various aspects of the software supply chain, such as the management of source code.

In each track, ascending levels signify progressively strengthened security measures. While higher levels offer enhanced protection against supply chain threats, they also entail higher implementation expenses. Lower SLSA levels are tailored for easier adoption, albeit with relatively modest security assurances. SLSA 0 is occasionally applied to software lacking any SLSA level compliance.

The combination of tracks and levels provides a convenient framework for assessing whether the software satisfies particular criteria. For instance, labelling an artifact as meeting SLSA Build Level 3 communicates that the software was constructed adhering to industry-endorsed security practices, guarding against specific supply chain vulnerabilities.


## What Can SLSA Do For You?

Everyone involved in producing and consuming software, or providing infrastructure for software can leverage SLSA 

- For software producers, SLSA safeguards against tampering in the supply chain, reducing insider risks and ensuring intended delivery to consumers.
- Software consumers benefit from SLSA by assessing the security practices of the software they rely on, ensuring received software matches expectations.
- Infrastructure providers play a crucial role in establishing a secure software supply chain between producers and consumers by adopting SLSA.

Large and small organizations, Open source projects and software vendors can all use SLSA to ensure the risk of a supply chain breach is minimized and the authenticity and integrity of their supply chain and deliverables can be validated. 

## What SLSA Is Not 

While SLSA is crucial, it's only part of a comprehensive supply chain security strategy. Considerations beyond SLSA include ensuring code quality by assessing developers' adherence to secure coding practices. Additionally, while SLSA builds trust within trusted organizations, it doesn't address intentional malicious production. Lastly, SLSA levels for artifacts don't encompass their dependencies, necessitating a recursive application of SLSA for a comprehensive assessment.

## Way Forward 

We have seen how implementing SLSA can help build confidence in our software supply chains and ultimately our product. But before we can begin the application of SLSA, we would need to understand the key terminologies and practices associated with SLSA. This will be covered in the next blog in this series. We would explore key concepts such as *Builder*, *Provenance*, *Validations*, etc which would help us getting started with implementing SLSA. 









