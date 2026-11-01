# Awesome-Data-Clean-Room-Privacy-Preserving-Analytics

# Awesome-Data-Clean-Room-Privacy-Preserving-Analytics

**Top Data Clean Room Privacy Preserving Analytics (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on TEE-Based Collaboration, Federated Analytics, Differential Privacy & Self-Hosted Clean Room Infrastructure*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Clean Rooms & Privacy-Preserving Analytics**. These tools enable organizations to collaborate on sensitive datasets—matching audiences, measuring campaigns, and training models—without exposing raw data to partners—from fully managed cloud clean rooms with identity resolution to open-source TEE-based frameworks that give organizations control over their collaboration infrastructure.



**Examples** include Snowflake Data Clean Rooms, Habu (LiveRamp), InfoSum, Decentriq, Optable, Samooha, AWS Clean Rooms, Google Ads Data Hub, LiveRamp Safe Haven, and Epsilon Clean Room (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted clean rooms, federated analytics, and open privacy infrastructure. **Critical note**: The open-source landscape is emerging—**PrivacyGo Data Clean Room (PGDCR)** from TikTok is the most complete open-source TEE-based clean room, but it is limited to one-way collaboration and GCP . **pda** provides federated statistical algorithms for healthcare research, not advertising clean rooms . **Dhara** is a test-data generator, not a clean room itself . No open-source project matches Snowflake's managed workflows or InfoSum's decentralized matching at production scale.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Snowflake Data Clean Rooms](https://www.snowflake.com/en/data-cloud/workloads/collaboration/data-clean-rooms/)**

  **Native clean room** within Snowflake's AI Data Cloud. **Pricing**: **No additional Snowflake access fees** for clean room features—consumption-based credits apply; **30-day free trial with $400 in free credits** . **Free tier**: Trial only ($400 credits). **Best for**: Snowflake customers wanting governed collaboration without data movement—**trade-off**: requires Snowflake ecosystem; credit consumption scales with query volume.



- **[Habu (LiveRamp Clean Room powered by Habu)](https://www.liveramp.com/)**

  **Data clean room platform** for secure collaboration on combined datasets. **Pricing**: **Custom quote**; **no free trial, no free plan** . **Free tier**: None. **Best for**: advertisers and publishers wanting managed clean room collaboration—**trade-off**: no self-serve evaluation; quote-only.



- **[InfoSum](https://www.infosum.com/)**

  **Decentralized data collaboration** platform with **non-movement of data** architecture. **Pricing**: **No free trial, no freemium version** per TrustRadius ; quote-only. **Free tier**: None. **Best for**: organizations requiring strict data residency—**trade-off**: no trial; federated query latency (10–30s) higher than edge-based alternatives .



- **[Decentriq](https://www.decentriq.com/)**

  **Confidential computing clean room** platform. **Pricing**: Quote-only; limited public pricing data . **Free tier**: Not specified. **Best for**: enterprises prioritizing TEE-based confidentiality—**trade-off**: limited public pricing transparency.



- **[Optable](https://optable.co/)**

  **Edge-computing clean room** with built-in identity graph for advertising. **Pricing**: Quote-only. **Free tier**: Not specified. **Best for**: publishers wanting low-latency audience activation (match rates 85–95%, query latency <5s) —**trade-off**: advertising-focused; less suited for multi-party consortia.



- **[AWS Clean Rooms](https://aws.amazon.com/clean-rooms/)**

  **Managed clean room** within AWS. **Pricing**: **Consumption-based**—compute measured in **Clean Rooms Processing Unit (CRPU)-hours**, per-second with 10-minute minimum; **no upfront costs**; **AWS Free Tier not available for Clean Rooms ML** . **Free tier**: None for ML. **Best for**: AWS-centric organizations wanting managed clean rooms—**trade-off**: CRPU consumption requires volume modeling.



- **[Google Ads Data Hub](https://adsdatahub.google.com/)**

  **Clean room for Google media measurement**. **Pricing**: **Free for Google media**; Cloud costs apply for queries . **Free tier**: Free for Google media measurement. **Best for**: advertisers measuring Google campaigns—**trade-off**: Google ecosystem lock-in; pricing transparency scored 1.0/5 .



- **[LiveRamp Safe Haven](https://liveramp.com/)**

  **Privacy-preserving data collaboration** environment. **Pricing**: Quote-only . **Free tier**: None. **Best for**: LiveRamp customers wanting clean room collaboration—**trade-off**: tied to LiveRamp ecosystem.



- **[Epsilon Clean Room](https://www.epsilon.com/emea/products-and-services/clean-room)**

  **Clean room with pre-loaded data and identity**. **Features**: **46M unique UK individuals** anchored in name and address; closed-loop cross-channel measurement; person-based activation . **Pricing**: Quote-only. **Free tier**: None. **Best for**: UK marketers wanting pre-enriched data on day one—**trade-off**: Epsilon data dependency; quote-only.



- **[Samooha](https://www.samooha.io/)**

  **Snowflake-native clean room** platform. **Pricing**: Quote-only. **Free tier**: Not specified. **Best for**: Snowflake customers wanting a third-party clean room interface—**trade-off**: limited public information in search results.



## Open-Source GitHub Projects



- **[PrivacyGo Data Clean Room (PGDCR)](https://github.com/tiktok-privacy-innovation/PrivacyGo-DataCleanRoom)**

  **Open-source TEE-based data clean room** (Apache-2.0) — **the most complete open-source clean room framework** found in this research, open-sourced by TikTok in June 2024 . **Features**: **Two-stage architecture**—Programming Stage (data exploration with provider-controlled protection) and Execution Stage (isolated TEE workload with attestation); **data providers manage data, code, and output space**; **JWT-based attestation** for public verification of execution integrity; **multi-cloud support** (currently GCP backend) . **Use cases**: Trusted Research Environments (TREs), advertising lookalike analysis, private ML model fine-tuning . **Tech stack**: Confidential Computing, GCP. **Deploy**: Self-hosted on cloud infrastructure. **Trade-off**: **Limited to one-way collaboration**—multi-user collaboration on roadmap; **manual data provisioning, policy, and attestation**—automation planned; **CPU-only**—GPU support planned . **Best for**: organizations wanting a TEE-based clean room they control—especially research institutions and privacy-focused data collaborations willing to accept early-stage limitations.



- **[pda: Privacy-Preserving Distributed Algorithms](https://cran.r-project.org/web/packages/pda/index.html)**

  **R package for federated statistical learning** (Apache-2.0) — **the most mature open-source federated analytics toolkit** for healthcare research . **Features**: **Regression, trial emulation, causal inference, clustering** across multiple data sites; **runs on a lead site** and requires only **summary statistics** from collaborating sites; **one or few iterations** for lossless results; integrates with **online data transfer system** for safe collaboration . **Tech stack**: R (Rcpp). **Deploy**: R package (CRAN). **Trade-off**: **Statistical research focus**—not advertising clean rooms or audience matching; requires R expertise. **Best for**: healthcare researchers and biostatisticians wanting federated analytics across institutions without sharing patient-level data.



- **[Dhara](https://pypi.org/project/vasundhara/)**

  **Synthetic multi-party dataset generator for clean room testing** (PyPI) — **the most practical open-source tool for clean room development** . **Features**: Generates **N CSV files** (one per data partner) with controlled **match ID overlap** via pairwise match rate matrix; **realistic column distributions** (categorical, integer, email, etc.); **match rate verification** in metadata; **schema inference** from CSV samples; **Audience Simulator** to preview filter impact; **reproducible via seed** . **Tech stack**: Python. **Deploy**: `pip install vasundhara`; CLI or Docker web UI. **Trade-off**: **Test data generator, not a clean room**—it helps you build and test clean rooms but does not perform privacy-preserving matching itself. **Best for**: developers building or evaluating clean room implementations—the essential testing companion for PGDCR or custom clean rooms.



### Additional Strong Open-Source Options



- **No mature open-source advertising clean room exists beyond PGDCR.** The commercial market (Snowflake, Habu, InfoSum, Optable) is proprietary, and open-source alternatives are either TEE frameworks (PGDCR) or research tools (pda). **Dhara** fills the testing gap but not the runtime gap.



**Frameworks for building custom systems**: Combine **PrivacyGo Data Clean Room** for TEE-based collaboration with **Dhara** for test data generation and **pda** for federated statistical analysis—creating a limited open-source clean room stack. **None of these match Snowflake's managed workflows or InfoSum's decentralized matching at production scale.**



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Data clean rooms handling customer data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate privacy-enhancing technologies (TEEs, differential privacy, secure multi-party computation).

- **The "managed clean room" vs. "TEE framework" vs. "federated analytics" vs. "test generator" distinction is critical.** **Snowflake, Habu, InfoSum, Optable, AWS, Google, LiveRamp, and Epsilon** are **managed clean rooms**—they provide hosting, identity resolution, and workflows . **PrivacyGo Data Clean Room** is a **TEE framework**—it provides the secure execution environment but requires manual setup and currently supports only one-way collaboration . **pda** is **federated analytics**—it enables statistical learning across sites, not advertising matching . **Dhara** is a **test generator**—it creates synthetic data for clean room development, not runtime collaboration . **Choose based on whether you need managed convenience, TEE control, statistical federation, or testing support.**

- **PrivacyGo Data Clean Room is the only open-source TEE clean room**, but it is **limited to one-way collaboration** and requires **manual provisioning, policy, and attestation**—automation is on the roadmap . **For organizations wanting TEE-based clean rooms today, it is the starting point; for production multi-party collaboration, commercial platforms are required.**

- **InfoSum and Optable have fundamentally different architectures.** InfoSum uses **decentralized non-movement of data** with federated queries (10–30s latency, 90–99% match rates). Optable uses **edge-computing with a local identity graph** (<5s latency, 85–95% match rates) . **Choose InfoSum for strict data residency; choose Optable for low-latency publisher-advertiser activation.**

- **Snowflake's clean rooms have no additional access fees**—you pay only for compute credits, with **$400 free trial credits** . **This is the most transparent pricing model in the managed clean room category.**

- **Habu (LiveRamp) has no free trial or free plan** . **InfoSum has no free trial or freemium version** . **Evaluation requires sales engagement.**

- **AWS Clean Rooms ML is not covered by AWS Free Tier** . **Google Ads Data Hub is free for Google media but Cloud costs apply** . **Budget for consumption costs even on "free" platforms.**

- **Pricing opacity is universal** across Habu, InfoSum, Decentriq, Optable, Samooha, and Epsilon. All require sales contact or quote requests. **Snowflake, AWS, and Google publish consumption-based pricing.** **Validate with direct vendor conversations against your collaboration volume and partner count.**

- Self-hosted open-source solutions require proper infrastructure (GCP for PGDCR, R for pda), security hardening for TEE attestation, and ongoing maintenance. **Clean rooms handle sensitive customer data**—ensure your deployment meets your organization's privacy and compliance requirements before onboarding partners.



---



**Made for data collaboration teams, privacy engineers, and organizations building transparent clean room solutions.**

Let's make Data Clean Rooms & Privacy-Preserving Analytics more open, data-driven, and privacy-safe.
