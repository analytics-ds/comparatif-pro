---
title: "Electronic invoicing in France: the complete 2026 guide"
description: "Complete guide to electronic invoicing in France: 2026-2027 reform, PPF, PDP, Factur-X, UBL, CII formats, e-reporting, penalties and compliance."
date: 2026-05-07
lastmod: 2026-05-07
publishDate: 2026-05-07
draft: false
categories: ["Business services"]
tags: ["e-invoicing", "2026-reform", "small-business", "sme", "tax-authority", "factur-x", "pdp"]
translationKey: "guide-facturation-electronique"
author: aurelie-vasseur
image: "/images/blog/guide-facturation-electronique.jpg"
imageAlt: "Diagram of electronic invoicing in France and its regulatory ecosystem"
imageCredit: "Image from Openverse (CC BY)"
faq:
  - question: "What is electronic invoicing in 2026?"
    answer: "It is a mandatory framework instituted by ordinance no. 2021-1190 of 15 September 2021 and decree no. 2022-1299 of 7 October 2022. Every invoice between VAT-registered taxpayers established in France must be transmitted in a structured format (Factur-X, UBL or CII compliant with EN 16931) via the Public Invoicing Portal or a partner dematerialization platform. The mechanism includes an obligation to transmit data (e-reporting) for B2C and international transactions."
  - question: "What are the key dates of the 2026-2027 timeline?"
    answer: "On 1 September 2026, every business established in France must be able to receive dematerialized invoices. On the same date, large enterprises and intermediate-size enterprises must issue their invoices in structured format and transmit their e-reporting data. On 1 September 2027, the issuance obligation extends to small and medium-sized enterprises and microenterprises (very small businesses, self-employed)."
  - question: "What is a PDP and is it necessary to choose one?"
    answer: "A partner dematerialization platform is a private operator registered by the French tax authority (DGFiP). It transmits structured invoices and e-reporting data between taxpayers and the tax administration. Using a PDP is not mandatory, the Public Invoicing Portal remains free of charge, but a PDP brings additional services (ERP connectors, evidential archiving, approval workflows, proprietary EDI formats)."
  - question: "Which formats are allowed?"
    answer: "Three core formats are accepted: Factur-X (PDF/A-3 with embedded XML data), UBL 2.1 (Universal Business Language) and UN/CEFACT CII (Cross Industry Invoice). All three comply with the European EN 16931 standard. A PDP may convert a proprietary EDI format to one of these three before transmission."
  - question: "What are the penalties for non-compliance?"
    answer: "Article 1737 of the French General Tax Code provides for a fine of 15 euros per non-compliant invoice, capped at 15,000 euros per calendar year, for failure to issue in electronic format. Failure to transmit e-reporting data is sanctioned by a 250 euros fine per omitted transmission, capped at 45,000 euros per year. Beyond financial penalties, the company is exposed to the risk of a VAT reassessment."
---

The generalization of electronic invoicing is reshaping the relationship between French companies and the tax administration. Adopted by ordinance no. 2021-1190 of 15 September 2021 and detailed by decree no. 2022-1299 of 7 October 2022, the reform introduces structured, standardized and traceable transmission of every commercial document between VAT-registered taxpayers. This complete 2026 electronic invoicing guide details the legal framework, the official timeline, the actors involved, the formats and the practical compliance steps.

> **In short:**
> 1. The reform rests on two pillars, the mandatory issuance of dematerialized structured-format invoices between French taxpayers, and the transmission of tax data (e-reporting) for B2C transactions, B2BIE flows and certain service payments.
> 2. Official timeline confirmed by the 2024 Finance Act (article 91): generalized reception by 1 September 2026, progressive issuance from 1 September 2026 (large enterprises, ETI) to 1 September 2027 (SMEs, very small businesses, microenterprises).
> 3. Three core formats are recognized: Factur-X (PDF + XML), UBL 2.1 and UN/CEFACT CII, all aligned with the European EN 16931 standard.
> 4. Non-compliance triggers a 15 euros fine per document, capped at 15,000 euros per year, without prejudice to the risk of a VAT reassessment.

## Definition and scope of electronic invoicing

Electronic invoicing refers to the issuance, transmission and reception of invoices in an exclusively digital form, using a structured or semi-structured format that allows automated processing. European directive 2014/55/EU and the **EN 16931** standard published by the European Committee for Standardization (CEN) laid the technical foundations for interoperability between European business information systems. France transposed this base into its domestic law through article 289 bis of the General Tax Code, introduced by the 2020 Finance Act and rewritten following the 2021 ordinance.

The scope covers every transaction between two VAT-registered taxpayers established in France (so-called domestic B2B transactions). Sales to end consumers (B2C), cross-border transactions (B2BIE for Business to Business International and Extracommunity) and intra-community acquisitions remain outside the issuance obligation but fall within the complementary data transmission mechanism, e-reporting.

For a deeper dive into the precise obligations depending on company status, read the [complete guide to mandatory electronic invoicing](/en/blog/mandatory-electronic-invoicing/).

## Legal context and history of the reform

The reform is part of a broader European movement to fight VAT fraud and modernize tax administration. The estimated annual revenue gap for French public finances, the **VAT gap**, reached almost 13 billion euros in 2020 according to the European Commission. Automated, near real-time transmission of invoicing data is designed as a key lever to reduce that gap, drawing on existing systems in Italy (**Sistema di Interscambio**, since 2019) and Spain (**SII**).

The schedule initially set by article 153 of the 2020 Finance Act planned implementation between 2024 and 2026. A postponement was announced by a French tax authority (DGFiP) press release on 28 July 2023, to consolidate the technical building blocks of the Public Invoicing Portal. The **2024 Finance Act**, in its article 91, finally enacted the new 2026-2027 timeline.

> "All persons subject to value added tax established in France will be required to accept electronic invoices as of 1 September 2026. The issuance obligation will apply on the same date to large enterprises and intermediate-size enterprises, then on 1 September 2027 to small and medium-sized enterprises and microenterprises."
> -- Article 91 of Act no. 2023-1322 of 29 December 2023, French Finance Act for 2024, Legifrance

Ordinance no. 2021-1190 of 15 September 2021 remains the founding text. Implementing decree no. 2022-1299 of 7 October 2022, supplemented by an order of the same date, sets the technical characteristics (formats, mandatory data, transmission terms), the registration conditions for partner dematerialization platforms (PDPs) and the rules for life-cycle status management. The **BOFIP** (official tax bulletin) publishes the related administrative doctrine under reference BOI-TVA-DECLA-30, with regular updates.

## Official timeline: 2026 and 2027 deadlines

The deployment schedule unfolds in two distinct waves for issuance, while the reception obligation applies simultaneously to all companies on 1 September 2026. This split allows smaller structures to take an extra year to adapt their tools, while ensuring they can still receive invoices from larger partners from day one.

| Deadline | Concerned audience | Reception | Issuance | E-reporting |
|---|---|---|---|---|
| 1 September 2026 | All companies established in France | Mandatory | Depending on size (see rows below) | Depending on size |
| 1 September 2026 | Large enterprises (over 5,000 employees or over 1.5 billion turnover) | Mandatory | Mandatory | Mandatory |
| 1 September 2026 | Intermediate-size enterprises (ETI, 250 to 4,999 employees) | Mandatory | Mandatory | Mandatory |
| 1 September 2027 | Small and medium-sized enterprises (SME, 10 to 249 employees) | Mandatory (since 2026) | Mandatory | Mandatory |
| 1 September 2027 | Microenterprises and very small businesses (under 10 employees) | Mandatory (since 2026) | Mandatory | Mandatory |
| 1 September 2027 | Self-employed (micro-fiscal and micro-social regime) | Mandatory (since 2026) | Mandatory | Mandatory |

The classification of companies follows decree no. 2008-1354 of 18 December 2008, combining headcount, turnover and balance sheet thresholds. Details and anticipation tips are developed in the dedicated [e-invoicing reform deadlines](/en/blog/electronic-invoicing-timeline/) page.

## Key actors: DGFiP, PPF, PDP, OD and OC

The target architecture follows a Y-shaped scheme. At the center, the **DGFiP** operates the Public Invoicing Portal and concentrates invoicing data for tax purposes. On the left, the issuer submits invoices either directly to the PPF or via a partner dematerialization platform (PDP). On the right, the recipient retrieves the invoices through the channel of its choice.

The **Public Invoicing Portal** (portailpro.gouv.fr), operated by the **French agency for state financial IT** (AIFE) and built on the Chorus Pro platform, plays a triple role: central directory of companies and their reception channels, free transit platform for issuers without a PDP, and data concentrator for the tax administration.

A **partner dematerialization platform** (PDP) is a private operator registered by the DGFiP after a qualification procedure (technical and security requirements, audit, service commitment). By Q1 2026, more than a hundred candidates had filed an application and several dozen were already provisionally or definitively registered. The official list is maintained on the DGFiP website. Choosing a PDP relies on coverage, robustness and integration criteria, detailed in the [partner dematerialization platform (PDP)](/en/blog/pdp-electronic-invoice/) page.

Two satellite actors round out the ecosystem. **Dematerialization operators** (OD) act upstream of a PDP or the PPF, without transmitting directly to the tax administration. **Concentrator operators** (OC), sometimes called trusted third parties, aggregate the flows of several companies before forwarding them to a PDP. The [role of the DGFiP in electronic invoicing](/en/blog/electronic-invoicing-dgfip/) describes the precise responsibilities of each link.

## Accepted formats: Factur-X, UBL, CII

Decree no. 2022-1299 retains three core formats, all compatible with the European EN 16931 standard. A PDP may accept other formats as input (proprietary EDI, sectoral GS1 EANCOM, EDIFACT, X12) provided it converts them to one of the three core formats before transmission to the PPF.

| Format | Type | Specificity | Preferred use case |
|---|---|---|---|
| Factur-X | Hybrid PDF/A-3 + embedded XML | Keeps a readable PDF visual, with structured XML CII data attached | Very small businesses, SMEs, sectors used to PDF, smooth transition |
| UBL 2.1 | Pure XML (Universal Business Language) | OASIS standard, widespread in Northern Europe and the United Kingdom | International B2B exchanges, advanced ERP integration |
| UN/CEFACT CII | Pure XML (Cross Industry Invoice) | UN standard, rich in logistics data | Industry, supply chain, sectors with extended data |

The **Factur-X** format is designed to ease adoption by very small businesses and SMEs, preserving human readability through PDF while offering an XML layer processable by IT systems. It is a Franco-German convergence with the **ZUGFeRD** format, version 2.1 of which is technically equivalent. For a detailed analysis of each format, read the [Factur-X, UBL and CII formats comparison](/en/blog/electronic-invoice-format-factur-x-ubl-cii/).

## Companies concerned: from large groups to self-employed

The scope is deliberately broad: every taxpayer registered for VAT in France falls within the reform. Specificities relate to differential application dates by size and to a few highly targeted exclusions (transactions exempt under article 261 of the General Tax Code, certain banking and insurance operations).

**Large enterprises** and **ETI** are on the front line on 1 September 2026. Their information systems, often built around a central ERP (SAP, Oracle, Microsoft Dynamics, Sage X3) and legacy EDI connectors, must be linked to a PDP or the PPF, and their internal validation cycles (entry, control, approval, accounting) must be adapted.

**SMEs** have an extra year. The risk for these structures lies mostly in the diversity of situations: some already have an integrated ERP, others still rely on Excel-based bookkeeping or a standalone invoicing tool. The [SME compliance with electronic invoicing](/en/blog/electronic-invoicing-sme/) page details an adapted compliance methodology.

**Very small businesses** and **self-employed** form the most heterogeneous segment. Software vendors targeting very small businesses (EBP, Henrri, Tiime, Indy, Pennylane, Quickbooks) massively integrated Factur-X into their offerings during 2024-2025. The PPF will remain free, allowing a microenterprise without dedicated software to issue its invoices through a public web portal. The [e-invoicing for very small businesses](/en/blog/electronic-invoicing-very-small-business/) page lists the most economical paths, and specifics of the micro-fiscal regime are detailed in the [reform and self-employed](/en/blog/electronic-invoicing-self-employed/) page.

## E-reporting: data transmission for B2C, B2BIE and payments

Alongside the domestic B2B invoice flow, the reform introduces an obligation to transmit data for the benefit of the tax administration, e-reporting. Three categories of data are concerned, corresponding to transactions not covered by the mandatory issuance of dematerialized invoices.

**Transaction e-reporting** covers B2C sales made by French taxpayers, B2BIE transactions (sales to or purchases from abroad), exports and intra-community acquisitions. The data to transmit include the total amount excluding tax, the VAT amount per rate, the nature of the transaction, the date and the customer's country. The frequency varies according to the VAT regime (monthly under the actual normal regime, quarterly under the simplified regime).

**Payment e-reporting** concerns services subject to VAT on receipt of payment (taxable event at the time of payment, not invoicing). It covers the date of receipt, the amount and the chargeable VAT, allowing the administration to reconcile chargeable VAT with collected VAT declared in returns.

**International B2B transaction e-reporting** targets flows between taxpayers that do not transit through the PPF, particularly when a supplier or customer is established outside France. The mechanism partially replaces the trade in goods declaration and the European declaration of services for the relevant flows.

All e-reporting data transit through a PDP or the PPF, in standardized formats distinct from invoices (specific XML schemas published by the DGFiP).

## Penalties and compliance

The penalty system, codified in article 1737 of the French General Tax Code and supplemented by articles 1788 D (e-reporting) and 1788 D bis (breaches of platform obligations), provides for fines on issuers, recipients and platforms alike. The logic is graduated: the fine is capped, but it adds to ordinary penalties in case of a VAT reassessment.

For the **issuer**, failing to issue in electronic format triggers a 15 euros fine per invoice, capped at 15,000 euros per calendar year. Failing to transmit e-reporting data exposes to a 250 euros fine per omitted transmission, capped at 45,000 euros per year. For the **recipient**, refusing without justification to receive a compliant electronic invoice is sanctioned by a 15 euros fine per invoice, capped at 15,000 euros per year. For the **PDP**, serious breaches may lead to suspension or withdrawal of registration.

Beyond specific penalties, non-compliance can call into question the right to deduct VAT if the invoice does not comply with mandatory mentions, or if it is not archived under the conditions of article L. 102 B of the Tax Procedures Code (six years, on tamper-proof electronic media). Several mandatory mentions deserve particular attention: SIREN of issuer and recipient, address of head office and place of delivery, exact nature of goods or services, applicable VAT rate per line, payment terms and late payment penalty rate. Any omission or inaccuracy on these mentions can be sanctioned and may, beyond the specific fine, also justify a denial of the right to deduct on the recipient side.

The administrative doctrine published by BOFIP under reference BOI-TVA-DECLA-30 details how the various penalties interact. The DGFiP has indicated, on impots.gouv.fr, that an indulgent approach will be applied during the first months of the ramp-up, with priority given to support and remediation rather than immediate sanctions for businesses acting in good faith. This communication does not, however, constitute a formal moratorium and the sanctions remain legally enforceable from the deadline.

## Practical compliance tips

A successful compliance approach rests on four structured steps, where the sequence matters as much as the content.

**Step 1: map the invoicing flows.** List the volumes (issued customer invoices, received supplier invoices), distinguish B2B France, B2C and B2BIE flows, identify current channels (paper, PDF by email, EDI, customer portal). This snapshot becomes the basis for tool selection.

**Step 2: audit the information system.** Check the ability of the current ERP or invoicing software to generate Factur-X, UBL or CII. Identify the modules to upgrade (VAT setup, country code table, subcontractor management, approval cycles). List the required integrations (CRM, document management, banking). Choosing an [electronic invoicing software for 2026](/en/blog/best-electronic-invoicing-software/) suited to the size and sector frames everything that follows.

**Step 3: choose the transmission channel.** The free PPF is enough for the simplest structures, with no significant volume or ERP integration. A PDP becomes relevant as soon as there is significant volume (more than a few hundred invoices per month), advanced accounting integrations, evidential archiving needs or sector constraints (health, construction, distribution with EDI). The [comparison of electronic invoicing platforms](/en/blog/electronic-invoicing-platforms-comparison/) details the selection criteria.

**Step 4: pilot and switch over.** Run a pilot phase on a restricted scope (a key customer, a subsidiary, a side activity), validate the full cycle (issuance, transmission, reception, accounting integration, archiving), identify anomalies, then generalize progressively. Waiting until the deadline is risky: the closer to 1 September 2026 or 2027, the higher the risk of bottlenecks at vendors and PDPs.

The tax administration provides evolving documentation on impots.gouv.fr, free training sessions through the chambers of commerce and professional bodies, and a dedicated support service for technical questions related to the PPF.

## Articulation with paper invoices and unstructured PDF

During the transition phase, several media coexist. A paper invoice remains valid between a French taxpayer not yet subject to the issuance obligation (before its application date of 1 September 2027 for very small businesses) and a recipient required to receive it. An unstructured PDF, without an XML layer, is no longer considered an electronic invoice within the meaning of the reform: it does not satisfy the obligation, even if electronically signed.

To avoid ambiguities, the administration recommends using exclusively Factur-X (PDF + embedded XML) for issuers wishing to keep a visual representation. This approach offers double readability: the recipient can display the PDF if needed, and its information system can directly process the XML.

Evidential archiving requires retention for six years from the date of the last transaction mentioned. Structured invoices must be retained in a format compliant with the eIDAS regulation and with the Code of relations between the public and the administration. A PDP usually offers an evidential archiving service included or as an option. The choice between internal and outsourced archiving depends on the volume of documents, on internal IT capabilities and on the existence of a third-party archiver already approved within the company. Documentary integrity must be guaranteed by qualified electronic signatures, qualified time-stamping or by retention on a write-once support.

Particular attention should be paid to flows with the public sector. Invoices issued to the State, local authorities and public institutions transit since 2017 through Chorus Pro, which has been integrated as a component of the Public Invoicing Portal. Companies invoicing public buyers must therefore verify that their solution properly handles the specific identifiers of public entities (SIRET, recipient services code) and the additional metadata required by the public order code.

## Institutional resources and doctrine updates

Tax doctrine evolves rapidly, given the technical nature of the reform and the ramp-up phase of platforms. Several institutional sources concentrate up-to-date information: impots.gouv.fr (DGFiP) gathers official documentation, portailpro.gouv.fr describes how the PPF works, BOFIP publishes the administrative doctrine under reference BOI-TVA-DECLA-30, Legifrance hosts ordinance no. 2021-1190, decree no. 2022-1299 and the 2024 Finance Act.

For an educational view of the framework, also consult the dedicated **service-public.fr** page and the briefs published by the **DGE** (French general directorate for enterprises) on economie.gouv.fr. The Comparatif-Pro pages that detail each facet of the framework rely on these sources, articulated around this pillar guide and complemented by sector-specific analyses (SMEs, very small businesses, self-employed, PDP selection, format selection).

## FAQ

<details>
<summary>What is electronic invoicing in 2026?</summary>

It is a mandatory framework instituted by ordinance no. 2021-1190 of 15 September 2021 and decree no. 2022-1299 of 7 October 2022. Every invoice between VAT-registered taxpayers established in France must be transmitted in a structured format (Factur-X, UBL or CII compliant with EN 16931) via the Public Invoicing Portal or a partner dematerialization platform. The mechanism includes an obligation to transmit data (e-reporting) for B2C and international transactions.
</details>

<details>
<summary>What are the key dates of the 2026-2027 timeline?</summary>

On 1 September 2026, every business established in France must be able to receive dematerialized invoices. On the same date, large enterprises and intermediate-size enterprises must issue their invoices in structured format and transmit their e-reporting data. On 1 September 2027, the issuance obligation extends to small and medium-sized enterprises and microenterprises (very small businesses, self-employed).
</details>

<details>
<summary>What is a PDP and is it necessary to choose one?</summary>

A partner dematerialization platform is a private operator registered by the French tax authority (DGFiP). It transmits structured invoices and e-reporting data between taxpayers and the tax administration. Using a PDP is not mandatory, the Public Invoicing Portal remains free of charge, but a PDP brings additional services (ERP connectors, evidential archiving, approval workflows, proprietary EDI formats).
</details>

<details>
<summary>Which formats are allowed?</summary>

Three core formats are accepted: Factur-X (PDF/A-3 with embedded XML data), UBL 2.1 (Universal Business Language) and UN/CEFACT CII (Cross Industry Invoice). All three comply with the European EN 16931 standard. A PDP may convert a proprietary EDI format to one of these three before transmission. More on the [EN 16931 standard](/en/blog/electronic-invoice-format-factur-x-ubl-cii/).
</details>

<details>
<summary>What are the penalties for non-compliance?</summary>

Article 1737 of the French General Tax Code provides for a fine of 15 euros per non-compliant invoice, capped at 15,000 euros per calendar year, for failure to issue in electronic format. Failure to transmit e-reporting data is sanctioned by a 250 euros fine per omitted transmission, capped at 45,000 euros per year. Beyond financial penalties, the company is exposed to the risk of a VAT reassessment.
</details>
