---
title: "PDP: partner dematerialization platform, role and selection | Comparatif-Pro"
translationKey: "pdp-facture-electronique"
date: "2026-05-07"
lastmod: "2026-05-07"
publishDate: "2026-05-07"
description: "PDP electronic invoice: definition, role, DGFiP certification, PDP/PPF/OD/OC distinctions, selection criteria and indicative list of certified vendors."
categories: ["Professional software"]
tags: ["pdp", "e-invoicing", "tax-authority", "ppf", "iso-27001", "directory", "certification"]
author: "thomas-durand"
image: "/images/blog/pdp-facture-electronique.jpg"
imageAlt: "Operator monitoring the routing of an electronic invoice through a certified partner dematerialization platform"
imageCredit: "Image from Openverse (CC BY)"
faq:
  - question: "What is a PDP in electronic invoicing?"
    answer: "A PDP (partner dematerialization platform) is a private operator certified by the French tax authority (DGFiP) to issue, transmit and receive digitised invoices between VAT-liable parties established in France. It also performs format conversion (Factur-X, UBL, CII), legally probative archiving for ten years, e-reporting of tax data and lifecycle status management. Without effective certification, a platform cannot act as a PDP under the reform."
  - question: "What is the difference between PDP, PPF, OD and OC?"
    answer: "The PPF (Public Invoicing Portal), operated by the AIFE, acts as the central directory and tax data hub for the DGFiP. The PDP is a private certified operator that transmits invoices and can also issue, receive, convert and archive them. An OD (dematerialization operator) provides digitisation services but is not certified, and therefore must rely on a PDP or the PPF for official transmission. An OC (communication operator) is a simple technical transporter of flows between two platforms, with no authority to act as an official issuer or recipient."
  - question: "How to verify that a PDP is certified?"
    answer: "The official register of certified PDPs is kept by the DGFiP and published on impots.gouv.fr. It lists the certification number, vendor name, issue date and validity period (three years, renewable). A platform that declares itself as 'in the process of certification' does not appear in the register until the procedure is finalised. A sound practice is to require, in the service contract, the disclosure of the actual certification number before any production rollout."
  - question: "How much does a PDP cost for an SME?"
    answer: "Pricing varies significantly with invoice volume, functional scope and accounting integrations. Entry offers start around 9 to 15 euros excl. VAT per month for a very small business issuing a few dozen invoices, and can exceed several thousand euros monthly for a multi-subsidiary mid-cap with ERP connectors, advanced archiving and EDI flows. Key drivers are monthly volume, number of users, number of legal entities and support level."
  - question: "Can a company use several PDPs at the same time?"
    answer: "Yes, nothing in decree 2022-1299 prevents a business from declaring multiple PDPs in the central directory: one for issuance, another for reception, or even different PDPs per subsidiary or per flow. The DGFiP directory handles such multi-platform configurations and tells the issuer which platform to target for each recipient. This flexibility remains rare in practice as it complicates archiving and steering. Most companies stick with a single PDP."
readingTime: true
---

The **pdp electronic invoice** designates the private operator certified by the French tax authority (DGFiP) that transmits digitised invoices between VAT-liable parties established in France. Together with the Public Invoicing Portal (PPF), the PDP forms the technical backbone of the reform brought by ordinance no. 2021-1190 and decree no. 2022-1299. From 1 September 2026, every domestic B2B invoice must transit through one of these platforms to be enforceable and feed the pre-filling of VAT returns.

Certification, governed by the order of 22 June 2023 setting out the PDP specifications, is far from a simple administrative formality. It requires an ISO 27001 security audit, validation by ANSSI (the French cybersecurity agency), a technical file aligned with DGFiP specifications, and the signature of a three-year renewable convention. This barrier to entry sets the PDP apart from other market players, in particular dematerialization operators (OD) and communication operators (OC) that do not share the same legal status.

> **Key points:**
> 1. A PDP is a private operator certified by the DGFiP, authorised to issue, transmit, receive, convert and archive digitised inter-business invoices.
> 2. Certification requires an ISO 27001 audit, ANSSI validation and compliance with the order of 22 June 2023, for an initial three-year period that can be renewed.
> 3. The PDP differs from the PPF (public directory and tax hub), the OD (not certified) and the OC (purely technical carrier).
> 4. The official register of PDPs is published by the DGFiP on impots.gouv.fr and is the only authoritative source for verifying the actual certification of a vendor.

## Definition of a partner dematerialization platform

A partner dematerialization platform is a private operator, certified by the Directorate General of Public Finance, that delivers transmission, conversion and archiving services for invoices on behalf of one or several VAT-liable companies. The legal status of the PDP is set out in article 290 B of the French Tax Code, introduced by the ordinance of 15 September 2021 and clarified by the decree of 7 October 2022.

Three features distinguish a PDP from a plain invoicing software vendor:

- Certification by the DGFiP, materialised by a unique number listed in the official register.
- The ability to transmit tax data directly to the public hub, without going through the PPF when both parties operate via certified PDPs.
- A binding contract covering specific obligations: data retention, service levels, incident reporting, compliance audits.

The PDP does not replace a company's accounting software or ERP. It plugs in downstream, either embedded in an accounting suite or as a connected service exposed via API. To grasp the broader context of the reform, the [complete electronic invoicing guide](/en/blog/electronic-invoicing-guide/) details every regulatory and technical building block.

> "Partner dematerialization platforms are one of the pillars of the target architecture. Their certification gives both businesses and the administration a high level of reliability, interoperability and security in their exchanges."
> -- Directorate General of Public Finance, impots.gouv.fr, 2024

## PDP vs PPF vs OD vs OC: four distinct actors

The dematerialization ecosystem rests on a chain of complementary actors. Mixing up PDP, PPF, OD and OC is a frequent mistake that can lead to a poor vendor choice or a compliance gap. The table below summarises the fundamental differences.

| Actor | Status | Main role | DGFiP certified | Can issue an official invoice |
|---|---|---|---|---|
| PPF (Public Invoicing Portal) | Public operator, run by the AIFE | Central directory, tax data hub, free fallback platform | Not applicable (public operator) | Yes |
| PDP (partner dematerialization platform) | Certified private operator | Issuance, transmission, reception, format conversion, legal archiving, e-reporting | Yes (official number, public register) | Yes |
| OD (dematerialization operator) | Non-certified private operator | Upstream or downstream digitisation services (capture, conversion, ERP integration) | No | No, must use a PDP or the PPF |
| OC (communication operator) | Non-certified private operator | Technical transport of flows between two platforms (EDI, API, AS4) | No | No, never acts as an official issuer or recipient |

The PPF, built on the Chorus Pro infrastructure and operated by the Agency for State Financial Information, plays three roles: central directory listing each business and its reception platform, hub for tax data sent to the DGFiP, and free fallback platform for entities that have not selected a PDP. The PDP, by contrast, is a private operator with extended services: user interfaces, accounting connectors, probative archiving, lifecycle status tracking, business reporting.

The OD positions itself upstream or downstream of the PDP. An accounting firm that scans and integrates supplier invoices without transmitting them directly to the PPF is a typical OD. The OC sits even further back: it carries flows between two platforms via protocols such as EDI, AS4 or specific APIs, without acting as an official issuer or recipient. The [tax administration's role in electronic invoicing](/en/blog/electronic-invoicing-dgfip/) clarifies the split of responsibilities between the administration and private operators.

## The PDP certification process

PDP certification by the DGFiP is governed by the order of 22 June 2023 setting out the specifications for partner dematerialization platforms. The process typically takes six to twelve months for a vendor that already has a compliance baseline in place, and may exceed eighteen months for a vendor building its compliance posture from scratch.

The certification dossier includes several blocks:

- Proof of registration in a French or European Union commercial register.
- A detailed description of the technical architecture, supported formats, supported protocols (REST API, EDI, AS4) and archiving arrangements.
- A security audit report delivered by a PASSI-qualified auditor or an accredited body, attesting to ISO 27001 compliance of the information system and adherence to ANSSI rules.
- A convention signed with the DGFiP, three years long and renewable, listing the operator's commitments on quality of service, incident notification and auditability.
- Compliance with rules on cleanliness, non-repudiation and traceability of flows, in line with the [electronic invoicing timeline](/en/blog/electronic-invoicing-timeline/).

The ISO 27001 audit covers the entire information security management system: risk mapping, access management, logging, business continuity plan, backups, subcontractor management. ANSSI validation focuses more specifically on cryptographic mechanisms (electronic signature, sealing, transmission encryption), the qualification of cryptographic modules and adherence to the General Security Reference framework.

Once the dossier is accepted, the DGFiP issues a certification number and lists the vendor in the official register on impots.gouv.fr. The initial duration is three years, with an interim audit at the midpoint. Any serious breach (loss of certification, failure to meet transmission obligations) leads to removal from the register and forces the affected PDP's clients to switch in haste to another operator or to the PPF.

## The operational functions of a PDP

A PDP is more than a pipe. The DGFiP specifications impose a substantial functional baseline that covers the full lifecycle of an invoice, from issuance to archiving, including the collection of tax data.

Eight structuring functions stand out:

- Issuance of an invoice compliant with the European standard EN 16931, in one of the standardised formats (Factur-X, UBL 2.1, CII).
- Transmission to the recipient through the channel listed in the central directory of the PPF, whether another PDP or the PPF itself.
- Reception of an incoming invoice with conformity check, signature verification and recipient notification.
- Format conversion when issuer and recipient use different formats, in accordance with the minimum data set defined by the DGFiP.
- Legally probative archiving for ten years, in line with article L102 B of the French Tax Procedures Book.
- E-reporting of payment data and operations not covered by electronic invoicing (B2C, international, intra-Community acquisitions).
- Lifecycle status management (deposited, received, accepted, rejected, paid), transmitted to the administration and to the partner.
- Continuous directory updates, to identify the recipient's reception platform at the moment of issuance.

The lifecycle status is one of the most structuring elements of the reform. Each transition is timestamped, signed and transmitted to the PPF, which forwards the information to both parties and the DGFiP. Status tracking allows an invoice to be traced end to end and provides evidence in disputes over a deadline or a payment.

## Standard journey of an invoice through a PDP

The standard issuance scenario via a PDP follows a sequence regulated by decree 2022-1299 and detailed in the external specifications published on impots.gouv.fr.

- Step 1: the issuer's accounting software produces the invoice in the pivot format (typically Factur-X) and sends it to its PDP via an API or connector.
- Step 2: the PDP checks the conformity of mandatory data (SIREN number, legal mentions, amounts, VAT codes) and electronically signs the invoice.
- Step 3: the PDP queries the central directory of the PPF to identify the recipient's reception platform (another PDP or the PPF).
- Step 4: the PDP transmits the invoice to the target platform via an interoperable channel (REST API, AS4, EDI under technical conventions).
- Step 5: the recipient platform receives the invoice, makes it available in its client interface and notifies the user.
- Step 6: the recipient issues a lifecycle status (received, accepted, partially or fully rejected), forwarded to the issuer and the DGFiP.
- Step 7: tax data (minimum data set) is extracted and sent to the public hub, which feeds the pre-filling of VAT returns.
- Step 8: the PDP archives the invoice for at least ten years, with timestamped sealing and an audit trail.

The whole journey is instrumented. A failed transmission triggers a traceable error status. A non-compliant format is rejected with a standardised error code. This mechanism aims to secure flows and improve VAT pre-filling reliability, in line with the anti-fraud objective embedded in the [comparison of electronic invoicing platforms](/en/blog/electronic-invoicing-platforms-comparison/).

## Certified vendors and candidates: indicative landscape

The official PDP register is a moving target. The first certification numbers were issued from 2024 onwards and the list grows with each round of audits. The table below offers an indicative landscape of vendors certified or in the certification process, to be checked systematically on impots.gouv.fr before any contract.

| Vendor | Indicative status | Main target | Notable feature |
|---|---|---|---|
| Pennylane | Certified | Very small businesses, SMEs | Unified accounting and invoicing approach, network of partner accountants |
| Sage | Certified | SMEs, mid-caps, large accounts | Native connector to Sage 100, Sage X3, Sage FRP 1000 suites |
| Cegid | Certified | SMEs, mid-caps, public sector | Integration with Cegid XRP, Cegid Quadra, Yourcegid |
| Yooz | Certified | Very small businesses, SMEs | Specialist in supplier invoice digitisation, intelligent capture |
| Esker | Certified | Mid-caps, large accounts | Cloud platform for order-to-cash and procure-to-pay cycles |
| Generix | Certified | Mid-caps, retail, supply chain | Strong EDI heritage, interoperability with logistics flows |
| Docaposte | Certified | Large accounts, public sector | Digital subsidiary of the La Poste group, recognised probative value |
| Iopole | In certification | Very small businesses, SMEs, accountants | Platform operated from France, sovereign positioning |
| Tiime | In certification | Very small businesses, SMEs, micro-entrepreneurs | Coupling of invoicing, accounting and banking services |
| EBP | In certification | Very small businesses, SMEs | Long-established French vendor with a wide installed base |
| Indy | In certification | Independents, liberal professions | Mobile application focused on simplified accounting |
| Axonaut | In certification | Very small businesses, small SMEs | All-in-one suite (CRM, quotes, invoicing, light accounting) |

Certification status can change quickly. A platform listed here is not necessarily certified at the time of reading, and the reverse is also true. For a broader overview of available solutions, the [best electronic invoicing software comparison](/en/blog/best-electronic-invoicing-software/) details features, prices and positioning, complementing the certification check carried out on impots.gouv.fr.

## Selection criteria for a PDP

Choosing a PDP cannot be reduced to certification alone. Functional and tariff gaps between operators are significant, and the decision commits a business for several years given migration costs, archiving duration and accounting integrations.

Seven criteria deserve close scrutiny:

- Effective certification, not a mere declarative status. Verify the number in the DGFiP register, request a copy of the three-year convention and the date of the latest ISO 27001 audit.
- Supported formats for issuance and reception: Factur-X, UBL 2.1, CII, and where needed ZUGFeRD or other sectoral profiles. A PDP that refuses a format may force a conversion that degrades the data.
- Accounting and ERP connectors: native integration with Sage, Cegid, EBP, Pennylane, SAP, Microsoft Dynamics, Oracle, Odoo. Connector quality drives operational fluidity and integration cost.
- Pricing: pricing grid by monthly volume, by user, by legal entity. Archiving costs, format conversion costs, premium support costs, initial onboarding fees.
- Support level: contractual SLAs, languages covered, time windows, critical incident handling, hands-on go-live support.
- Complementary certifications: NF525 for cash registers, eIDAS qualification for signature services, SOC 2 certification for internal controls, HDS approval if archiving covers health data.
- Product trajectory: documented roadmap, dedicated regulatory compliance teams, ability to track DGFiP evolutions (extended e-reporting, new statuses, ViDA continuous transaction control framework).

Sectoral context also weighs in. An industrial mid-cap will favour a PDP with strong EDI roots and a robust ERP connector. A small services business will lean towards a platform tightly coupled with a cloud accounting suite, with quick onboarding. An accounting firm will look for a multi-client PDP that fits into its production tooling and supports invoicing on behalf of third parties.

## Verifying certification: DGFiP register and directory API

Systematic verification of certification status is a basic compliance reflex. Two official tools confirm whether a vendor holds the rights required to act as a PDP.

The register of certified PDPs is published on impots.gouv.fr, in the section dedicated to electronic invoicing. For each operator it lists the trade name, SIREN number, certification number, issue date, validity period and functional scope. The register is freely consultable. It is the authoritative source in case of dispute: a vendor that does not appear cannot claim the status, even if it declares an ongoing process.

The directory API, published by the PPF and documented by the AIFE, allows PDPs, ERPs and accounting software to query continuously the list of recipients and their reception platform. This API enables automatic routing of an invoice to the right channel. It is updated near real time, freeing issuers from manually maintaining a supplier directory. The minimum functional baseline of a PDP includes regular querying of this API and updating of issuance and reception partners in its internal repository.

Three good practices complete the picture:

- Include a certification recall clause in the service contract with the PDP, requiring the vendor to notify any loss or suspension of its status without delay.
- Audit the PDP's presence in the register once a year, ideally tied to year-end closing or business continuity plan reviews.
- Verify that the PDP can publish, on request, its ISO 27001 audit evidence and SOC 2 or equivalent report, in addition to the certification number.

To anticipate format choices and contract negotiations, the [UBL and CII formats](/en/blog/electronic-invoice-format-factur-x-ubl-cii/) article details the technical specifics that any PDP must handle and explains the implications of the minimum data set required by the DGFiP.

## Risks of a poor PDP choice

A poor decision exposes the company to several risks, some immediate and others latent.

- Compliance risk: relying on a non-certified vendor presented as a PDP. Invoices issued or received via this operator are not enforceable under the reform and may be rejected in VAT pre-filling, triggering administrative chasing.
- Technical lock-in risk: vendor lock through proprietary formats or long-term contracts without a reversibility clause. Migrating from one PDP to another requires archive portability and access to lifecycle journals over ten years.
- Operational risk: recurring downtime, transmission delays, incidents not resolved within contractual timelines. A vague or undocumented SLA is a red flag.
- Tariff risk: complex pricing grids with hidden costs on peak volumes, format conversions or extra integrations. Budget comparison must be based on real-volume simulations, not theoretical averages.
- Legal risk: non-compliance with probative archiving obligations, failure to report incidents, breach of the DGFiP convention. A loss of certification triggered by a failed audit forces a rushed switch and may incur significant transition costs.

The safeguards are clear: register check, line-by-line contract analysis, migration simulation, documented business continuity plan, quarterly tracking of service quality indicators. Reviewing the legal corpus available on Legifrance, in particular the order of 22 June 2023 and article 41 of decree 2022-1299, frames the minimum requirements expected from a serious provider.

## Wrap-up: the PDP at the heart of the tax mechanism

The PDP is more than a technical subcontractor. It acts as a trusted third party between businesses and the DGFiP, secures the integrity and traceability of flows, and carries its own regulatory commitments. Selecting one deserves a strict analytical grid built on actual certification, the robustness of the functional baseline and the strength of the contract.

Three guideposts to structure the decision:

- Verify certification in the official register published on impots.gouv.fr, beyond any commercial declaration.
- Align the choice with business constraints: volumes, accounting integrations, sector, archiving, multi-country.
- Document contractual commitments (SLAs, audits, reversibility) and prepare a continuity plan should the chosen PDP fail.

To round out the picture and connect the PDP topic with the overall reform mechanics, the [electronic invoicing timeline](/en/blog/electronic-invoicing-timeline/) lays out the milestones of each obligation.

## FAQ

<details>
<summary>What is a PDP in electronic invoicing?</summary>

A PDP (partner dematerialization platform) is a private operator certified by the French tax authority (DGFiP) to issue, transmit and receive digitised invoices between VAT-liable parties established in France. It also performs format conversion (Factur-X, UBL, CII), legally probative archiving for ten years, e-reporting of tax data and lifecycle status management. Without effective certification, a platform cannot act as a PDP under the reform.
</details>

<details>
<summary>What is the difference between PDP, PPF, OD and OC?</summary>

The PPF (Public Invoicing Portal), operated by the AIFE, acts as the central directory and tax data hub for the DGFiP. The PDP is a private certified operator that transmits invoices and can also issue, receive, convert and archive them. An OD (dematerialization operator) provides digitisation services but is not certified, and therefore must rely on a PDP or the PPF for official transmission. An OC (communication operator) is a simple technical transporter of flows between two platforms, with no authority to act as an official issuer or recipient.
</details>

<details>
<summary>How to verify that a PDP is certified?</summary>

The official register of certified PDPs is kept by the DGFiP and published on impots.gouv.fr. It lists the certification number, vendor name, issue date and validity period (three years, renewable). A platform that declares itself as 'in the process of certification' does not appear in the register until the procedure is finalised. A sound practice is to require, in the service contract, the disclosure of the actual certification number before any production rollout.
</details>

<details>
<summary>How much does a PDP cost for an SME?</summary>

Pricing varies significantly with invoice volume, functional scope and accounting integrations. Entry offers start around 9 to 15 euros excl. VAT per month for a very small business issuing a few dozen invoices, and can exceed several thousand euros monthly for a multi-subsidiary mid-cap with ERP connectors, advanced archiving and EDI flows. Key drivers are monthly volume, number of users, number of legal entities and support level.
</details>

<details>
<summary>Can a company use several PDPs at the same time?</summary>

Yes, nothing in decree 2022-1299 prevents a business from declaring multiple PDPs in the central directory: one for issuance, another for reception, or even different PDPs per subsidiary or per flow. The DGFiP directory handles such multi-platform configurations and tells the issuer which platform to target for each recipient. This flexibility remains rare in practice as it complicates archiving and steering. Most companies stick with a single PDP.
</details>
