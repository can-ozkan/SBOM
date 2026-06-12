# Supply chain insecurity: Why SBOMs cannot be fully trusted

In this repo, all the artifacts can be found that we used during our paper. Additionally, the solutions folder contains the code we propose to mitigate the attack we consider.

# Abstract of the paper

The SolarWinds attack, which exploited weaknesses in a software update mechanism, highlights the critical need for organizations to have better visibility into their software dependencies and potential vulnerabilities associated with them. 
The Software Bill of Materials (SBOM) is paramount in ensuring software supply chain security. Under the Executive Order issued by President Biden, the adoption of the SBOM has become mandatory within the United States. SBOMs are being put forward as one of the key pillars in vulnerability management. In this paper, we investigate whether the output of SBOMs can be trusted under the
assumption that a so-called codebase attacker is present. Our research
reveals that the SBOM generation process across popular programming
languages is susceptible to stealthy manipulation, leading to significant
supply chain insecurities and organizations falsely believing that their
software assets are free from vulnerabilities. Our analysis also revealed
several security shortcomings in popular SBOM consumption tools. To
address these security issues, we analyze the use of public repositories for
software libraries to validate the integrity of the dependency information
within an SBOM and demonstrate the feasibility of this approach by a
proof-of-concept implementation.
