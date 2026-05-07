---
title: "Electronic invoice formats: Factur-X, UBL, CII explained"
translationKey: "format-facture-electronique-factur-x-ubl-cii"
date: "2026-05-07"
lastmod: "2026-05-07"
publishDate: "2026-05-07"
description: "Electronic invoice format: understand Factur-X, UBL and CII, their link with EN 16931, their differences and their role in the PPF and the PDPs."
categories: ["Professional software"]
tags: ["factur-x", "ubl", "cii", "en-16931", "pivot-format", "electronic-invoicing", "peppol"]
author: "thomas-durand"
image: "/images/blog/format-facture-electronique-factur-x-ubl-cii.jpg"
imageAlt: "Technical comparative diagram of Factur-X, UBL and CII formats based on the European EN 16931 standard for electronic invoicing"
imageCredit: "Image from Openverse (CC BY)"
faq:
  - question: "What are the three electronic invoice formats accepted in France from September 2026?"
    answer: "The reform stemming from decree 2022-1299 and the order of 22 June 2023 retains three mandatory syntaxes for the interoperability core: Factur-X, UBL and CII. All three must comply with the semantic reference of the European EN 16931 standard published by CEN. The PPF (Public Invoicing Portal) and every registered PDP (Partner Dematerialization Platform) must issue, receive and convert these three formats. Proprietary EDI flows remain marginally accepted between PDPs, but the translation to one of the three standardized formats remains mandatory at output."
  - question: "What is the difference between Factur-X and ZUGFeRD?"
    answer: "Factur-X and ZUGFeRD are two names for the same hybrid format, jointly developed by the Forum National de la Facture Electronique (FNFE-MPE) in France and the Forum elektronische Rechnung Deutschland (FeRD) in Germany. Versions 1.0 and above are aligned and technically interoperable. The Factur-X name is used in France and the ZUGFeRD name is used in Germany, but the EN 16931, BASIC, EXTENDED and MINIMUM profiles carry the same tags and the same embedded CII XML structure inside the PDF/A-3."
  - question: "Should you choose UBL, CII or Factur-X for your accounting software?"
    answer: "The choice depends on the context. Factur-X suits companies that want a gradual migration with human readability of the preserved PDF. UBL is favored in environments already tooled for Peppol or European e-commerce. CII remains the natural choice for large industrial groups and sectors where UN/CEFACT has historically dominated, such as automotive and large-scale retail. In any case, a properly registered PDP is required to ensure conversion between the three, so the initial choice is not locking."
  - question: "Does the EN 16931 standard impose a single technical format?"
    answer: "No. The EN 16931 standard, published by the European Committee for Standardization, defines a common semantic model, that is, the list of mandatory invoice information (identifier, dates, seller, buyer, lines, totals, VAT, contractual references). It does not freeze the XML syntax. Two syntaxes are recognized as compliant under the standard: UBL 2.1 (CEN/TS 16931-3-2) and CII 16B (CEN/TS 16931-3-3). Factur-X reuses the CII syntax embedded in a PDF/A-3."
  - question: "How does Peppol BIS Billing 3.0 fit relative to the French formats?"
    answer: "Peppol BIS Billing 3.0 is an implementation specification published by OpenPeppol AISBL, based on UBL 2.1 and compliant with EN 16931. It is already used as an exchange backbone by Nordic, Dutch and Belgian administrations. France does not make Peppol its official channel, but registered PDPs must guarantee interoperability with Peppol access points for inbound and outbound flows involving European partners already connected to the network."
readingTime: true
---

The **electronic invoice format** designates the way structured invoice data is serialized to be exchanged, read and archived by a machine. The reform stemming from ordinance no. 2021-1190 and decree no. 2022-1299 imposes an interoperability core resting on three mandatory syntaxes: Factur-X, UBL and CII. These three formats share the same semantic model, defined by the European EN 16931 standard published by the European Committee for Standardization (CEN).

This technical core conditions the circulation of dematerialized invoices within the Public Invoicing Portal and between registered PDPs. Without alignment on these syntaxes and on the EN 16931 semantics, no domestic B2B invoice can be validly transmitted from 1 September 2026. Accounting software publishers, ERPs, supplier portals and dematerialization operators must integrate this standardized base, and it is also on these formats that the automated checks of the tax administration will rely for VAT return pre-filling.

> **In brief:**
> 1. The European EN 16931 standard, published by CEN, defines the common semantic model for all dematerialized invoices in Europe.
> 2. Three syntaxes are retained as compliant: Factur-X (PDF/A-3 with embedded CII XML), UBL (pure XML from OASIS) and CII (pure XML from UN/CEFACT).
> 3. Factur-X favors human readability of the PDF, UBL is the dominant format of Peppol and European e-commerce, CII remains very present in industry and large groups.
> 4. PPF and PDPs must issue, receive and convert the three formats, which makes the initial choice reversible and infrastructure-side interoperability guaranteed.

## Why a standardized format for the dematerialized invoice

The objective of a standardized format is threefold: reduce the connection costs between systems, guarantee the auditability of tax data and allow the administration to pre-fill VAT returns. Without a common standard, each flow between two companies would require a tailor-made integration, as was the case in traditional EDI. The generalized dematerialization of invoices, on the contrary, imposes a single technical core recognized by all actors.

Standardization also plays an anti-fraud role. The DGFiP (French tax authority) concentrator receives identical structured data regardless of the transmitting PDP, which makes anomalies easier to detect automatically. Continuous transactional controls (CTC) rely precisely on this homogeneity: without a recognized pivot format, e-reporting and the transmission of B2B invoicing data could not be automated on a national scale. The same logic applies to B2G exchanges via Chorus Pro and to part of aggregated B2C.

The choice to align France with the European EN 16931 standard is explicit in decree 2022-1299 and in the PDP specifications. This facilitates intra-EU exchanges, avoids the creation of an isolated national dialect and capitalizes on tools already proven in the Peppol ecosystem and in administrations applying European directive 2014/55/EU on electronic invoicing in public procurement. To grasp the broader context, the [complete electronic invoicing guide](/en/blog/electronic-invoicing-guide/) details the entire setup.

> "The European EN 16931 standard establishes the semantic data model essential to the electronic invoice. It allows public and private buyers and suppliers in the European Union to exchange invoices in an automated manner."
> -- European Committee for Standardization (CEN), EN 16931-1 publication, 2017

## The European EN 16931 standard: a common semantic reference

Adopted in 2017 by CEN, the EN 16931 standard was developed in response to the M/528 mandate entrusted by the European Commission. It describes the semantic model of a basic electronic invoice, that is, the list of essential information items and their business meaning, without dictating the technical syntax of implementation. CEN distinguishes two levels: the core (core invoice model) and optional sectoral extensions.

The standard core contains around a hundred elements: identifiers, dates, seller, buyer, invoice lines, totals, VAT breakdown, contractual references, payment terms. Each element is documented with a cardinality, a data type and a business definition. The business rules (BR-XX) impose consistencies, for example the mandatory presence of a VAT identifier for taxable operations or the consistency between the sum of lines and the total excluding tax. This semantic grid serves as a common reference for the three technical formats retained in France.

EN 16931 is supplemented by several technical specifications, including CEN/TS 16931-3-2 (mapping to UBL 2.1) and CEN/TS 16931-3-3 (mapping to CII 16B). These two mappings explain how each semantic element translates into the XML tags of the two syntaxes. This logic makes the standard a conceptual pivot format: tools do not necessarily dialogue in EN 16931 directly, they dialogue in an XML syntax compliant under the standard. The [role of the DGFiP in electronic invoicing](/en/blog/electronic-invoicing-dgfip/) explains how this reference serves as the basis for automated controls.

## Factur-X: the hybrid PDF + XML format

Factur-X is a hybrid format developed in France by the Forum National de la Facture Electronique (FNFE-MPE) and AFNOR, jointly with Germany under the name ZUGFeRD. It combines two components in the same file: a PDF/A-3, readable by any human or office tool, and a CII XML file embedded as an attachment, exploitable by computer systems. Human reading and automatic processing are thus possible from the same document.

The major interest of Factur-X is to facilitate a gradual transition. A company that issues classical visual PDFs today can continue to archive PDFs while injecting structured data in CII format inside. The recipient who has not yet deployed an extraction tool reads the invoice as before, the equipped recipient automatically extracts the XML tags and integrates them into its ERP. The format is defined by the Factur-X 1.0.07 specification published in September 2024, aligned with the ZUGFeRD 2.3 version on the German side.

Factur-X recognizes several profiles, from the most minimalist to the richest: MINIMUM, BASIC WL, BASIC, EN 16931 (formerly COMFORT) and EXTENDED. From 1 September 2026, issuances to the PPF or via a PDP must at minimum use the EN 16931 profile, that is, comply with the entire core of the European standard. The MINIMUM and BASIC WL profiles, more restricted, remain authorized for special cases (invoice without VAT, simple recap). This evolution toward the EN 16931 profile is crucial and several accounting software publishers still need to align their versions, as detailed in the [electronic invoicing platforms comparison](/en/blog/electronic-invoicing-platforms-comparison/).

## UBL: Universal Business Language by OASIS

UBL, an acronym for Universal Business Language, is an open standard published by OASIS (Organization for the Advancement of Structured Information Standards). Version 2.1, standardized in ISO/IEC 19845:2015, is the basis of most current implementations, including Peppol BIS Billing 3.0 and Nordic implementations. UBL defines a set of XML schemas for the entire commercial cycle: order, delivery note, invoice, credit note, quote request.

UBL is a pure XML format, with no embedded visual content. Its syntax is verbose: each field carries a long, explicit name, which makes it quite readable for a developer, at the cost of a heavier payload than a compact format. The tags are structured by major blocks: `cbc:` for basic components, `cac:` for aggregate components, with a hierarchy that exactly mirrors the business concepts of the UBL model. This verbosity is offset by an excellent tooling ecosystem: open source libraries in nearly every language, public validators, visualization PDF generators.

The use of UBL is dominant in Nordic countries, the Netherlands, Belgium and more broadly wherever Peppol has taken root. For a French company already tooled for Peppol, for example because it delivers European public contracts, routing its domestic invoices in UBL via a PDP that supports this format limits specific developments. This continuity is a strong argument for many international SaaS publishers already established in France.

## CII: Cross Industry Invoice by UN/CEFACT

CII, for Cross Industry Invoice, is the XML syntax developed by UN/CEFACT, the United Nations Centre for Trade Facilitation and Electronic Business. Version 16B, published in 2016, is the one retained by France. CII is a pure XML format, more compact than UBL, whose structure derives from the UN/CEFACT exchange model for global supply chains. The tags are also explicit but often use business abbreviations stemming from international trade.

CII stands out for its industrial anchoring. Many large European groups, particularly in automotive, large-scale retail, aerospace and chemicals, have long used UN/CEFACT schemas for their EDIFACT flows and their XML evolutions. For these sectors, CII is the logical continuation of years of anti-fraud tooling and document traceability. This is also why Factur-X embeds CII and not UBL, even though Peppol bets on UBL: technical choices reflect the history of leading sectors.

CII is more compact than UBL in file size but often considered harder to read for a developer unfamiliar with it. Its learning curve is steeper, but its alignment with existing EDIFACT schemas allows teams already tooled for EDI to capitalize on their mappings. In the French context, the choice of CII is frequent among publishers targeting mid-cap and large industrial accounts. The [best electronic invoicing software](/en/blog/best-electronic-invoicing-software/) details format compatibility per publisher.

## Structural comparison of the three formats

The table below summarizes the main differences between Factur-X, UBL and CII. All three comply with the EN 16931 semantic model but differ in syntax, readability and preferred use context. None of the three syntaxes is excluded by the reform: PPF and PDPs must support all of them in issuance, reception and conversion.

| Criterion | Factur-X | UBL 2.1 | CII 16B |
|---|---|---|---|
| Type | Hybrid PDF/A-3 + embedded CII XML | Pure XML | Pure XML |
| Standard publisher | FNFE-MPE / AFNOR / FeRD | OASIS (ISO/IEC 19845:2015) | UN/CEFACT |
| EN 16931 compliant | Yes, EN 16931 profile mandatory from September 2026 | Yes, via CEN/TS 16931-3-2 | Yes, via CEN/TS 16931-3-3 |
| Human readability | Very high (visual PDF) | Low without viewer | Low without viewer |
| XML verbosity | Medium (inherited from CII) | High (long tags) | More compact than UBL |
| Ecosystem | France, Germany, PDF transition | Peppol, Nordic countries, Netherlands, Belgium | Industry, automotive, extended EDI |
| Preferred use case | Gradual migration with preserved PDF | Peppol environment or European e-commerce | Large industrial groups, UN/CEFACT sectors |
| Average file size | Equivalent to a PDF + compact XML | The largest of the three | The most compact |

A properly registered PDP is required to convert an invoice between the three formats without semantic alteration. Concretely, if a company issues in Factur-X and its client is equipped to consume only UBL, the recipient (or intermediary) PDP performs the automatic conversion. This format neutrality simplifies internal choices and avoids the historical EDI integration deadlocks.

## Semantic equivalence: same information, different syntaxes

In accordance with the CEN/TS 16931-3 specification, each business concept of the EN 16931 standard has a precise mapping to UBL and to CII. The concrete consequence is that the three formats carry the same useful information for a given invoice, simply encoded differently. The table below illustrates this equivalence on the main tags.

| EN 16931 concept | UBL 2.1 tag | CII 16B / Factur-X tag |
|---|---|---|
| Invoice number (BT-1) | `cbc:ID` | `ram:ID` (under `rsm:ExchangedDocument`) |
| Issue date (BT-2) | `cbc:IssueDate` | `udt:DateTimeString` (under `ram:IssueDateTime`) |
| Invoice type code (BT-3) | `cbc:InvoiceTypeCode` | `ram:TypeCode` (under `rsm:ExchangedDocument`) |
| Seller identifier (BT-31, VAT) | `cac:AccountingSupplierParty/cac:Party/cac:PartyTaxScheme/cbc:CompanyID` | `ram:SellerTradeParty/ram:SpecifiedTaxRegistration/ram:ID` |
| Buyer identifier (BT-48, VAT) | `cac:AccountingCustomerParty/cac:Party/cac:PartyTaxScheme/cbc:CompanyID` | `ram:BuyerTradeParty/ram:SpecifiedTaxRegistration/ram:ID` |
| Currency (BT-5) | `cbc:DocumentCurrencyCode` | `ram:InvoiceCurrencyCode` |
| Total amount excluding VAT (BT-109) | `cbc:TaxExclusiveAmount` | `ram:TaxBasisTotalAmount` |
| Total amount including VAT (BT-112) | `cbc:TaxInclusiveAmount` | `ram:GrandTotalAmount` |
| Invoice line (BG-25) | `cac:InvoiceLine` | `ram:IncludedSupplyChainTradeLineItem` |

A conversion tool compliant with CEN/TS 16931-3 specifications must guarantee that all tags listed in the standard are transposed without loss. This is what is called conversion without semantic deperdition. To go further, the public Schematron schemas provided by CEN allow validating that an XML invoice complies with EN 16931 regardless of the chosen syntax.

## Format choice depending on context

The format choice depends on several criteria: the company's current situation, its commercial partners, its ERP or accounting software and the PDP it has selected. Three major cases dominate French practice.

For a very small business or SME just emerging from paper or unstructured PDF invoicing, Factur-X is often the smoothest trajectory. The PDF remains readable by less-equipped clients, and the embedded CII XML ensures PPF compliance. Most consumer-facing publishers (Sage, EBP, Indy, Tiime, Henrri, Pennylane) have adopted this approach by default. This choice is also favored by accounting firms, which prefer a doubly readable document for their clients and for automated entry tools. The [electronic invoicing platforms comparison](/en/blog/electronic-invoicing-platforms-comparison/) shows that nearly all French platforms support Factur-X as standard.

For a company already connected to Peppol, or that delivers European public contracts via PEPPOL eDelivery, UBL is more natural. The dual implementation of Factur-X and UBL needlessly weighs down the chain. A PDP that supports UBL natively, for example via Peppol BIS Billing 3.0, avoids internal conversions. Major international publishers (Quickbooks, several SAP solutions, certain Sage modules) are aligned on UBL as a priority.

For a mid-cap or large industrial group already tooled for EDIFACT and CII, the move to pure CII is the logical continuation. The format lends itself well to high-volume flows with application envelope control and historical EDI requirements. This is notably the choice in automotive, large-scale retail and chemicals. For these structures, the risk is fragmenting flows between channels: the PDP must then be able to convert CII to Factur-X or UBL for less-equipped partners. The [Partner Dematerialization Platform (PDP)](/en/blog/pdp-electronic-invoice/) precisely plays this role of technical arbitrator.

## Formats accepted by the PPF and PDPs

The PDP specifications, published by the order of 22 June 2023, explicitly impose support for the three formats Factur-X, UBL and CII in issuance, reception and conversion. This obligation guarantees interoperability regardless of the issuer/recipient combination. The PPF, managed by the AIFE (French agency for state IT finance) and accessible via portailpro.gouv.fr, applies exactly the same support and conversion rules. No PDP can impose a single format on its users.

In practice, the issuer configures its output format in its accounting software or ERP, the issuer's PDP transmits, the PPF routes via the central directory, and the recipient's PDP eventually converts to the format the recipient has chosen to receive. The correspondence table and routing rules are described in the external specifications dossier published by the DGFiP. This transparency for the end user is one of the major achievements of the reform: no manual entry, no flow break between formats.

Proprietary EDI formats (EDIFACT, X12, sectoral formats) are tolerated between PDPs that have agreed bilaterally. But on output to the PPF or to the final recipient, conversion to Factur-X, UBL or CII remains mandatory. This rule limits the ecosystem's dependence on legacy EDI flows while preserving the existing investments of large accounts. The [complete electronic invoicing guide](/en/blog/electronic-invoicing-guide/) revisits this routing mechanism in detail.

## Upcoming evolutions: profiles, ZUGFeRD and Peppol

The three formats evolve in parallel. On the Factur-X side, version 1.0.07 published in September 2024 by the FNFE-MPE is the functional reference. A major expected evolution is the generalization of the EN 16931 profile by default on 1 September 2026, followed by a ramp-up of the EXTENDED profile for sectors imposing complex contractual references. On the ZUGFeRD side, version 2.3 published in autumn 2024 remains aligned with Factur-X and guarantees Franco-German compatibility for multi-country groups.

UBL evolves more slowly, version 2.1 having been frozen since 2013 and stabilized by ISO/IEC in 2015. The Peppol BIS Billing 3.0 specification, on the other hand, is the subject of regular updates by OpenPeppol AISBL to clarify validation rules, add country codes and adjust business rules. France, without making it its official channel, follows these evolutions for intra-EU interoperability. Several French PDPs, particularly the most international ones, have obtained their Peppol access certification alongside their DGFiP registration.

On the CII side, version 16B remains the reference, but UN/CEFACT is working on a 22B version expected around 2027. French tools will align following the CEN publications. In the meantime, the regulatory priority is compliance with the EN 16931 profile and respect for the public Schematron schemas. Accounting software publishers that have not yet aligned their versions risk an automatic rejection of their flows by the PPF after September 2026.

> "The interoperability core rests on three core formats (UBL, CII, Factur-X) and on respect for EN 16931 business rules. Any invoice exchanged through the PPF or a PDP must respect its semantics."
> -- Direction generale des Finances publiques, external specifications dossier, 2024

## Tools and publishers adopting the three formats

Several French and international publishers already support the three formats simultaneously, either directly or via their integrated PDP. Pennylane, Sage, Cegid, EBP, Yooz, Esker, Iopole, Generix, Docaposte and Tiime display full Factur-X support, and most offer UBL for Peppol flows and CII for large industrial accounts. Publishers oriented toward very small businesses and SMEs (Indy, Henrri, Axonaut) currently remain centered on Factur-X but announce UBL support in progress, generally backed by their partner PDP.

On the open source tooling side, several widely used libraries facilitate the generation and validation of compliant invoices. For Factur-X, the Factur-X.org library maintained by the FNFE-MPE is the Java/.NET reference. For UBL, OpenPeppol publishes Schematron schemas and starter kits. For CII, UN/CEFACT makes the official XSD schemas available via its website. These tools are used by most PDPs in addition to their own internal developments, as indicated in the [best electronic invoicing software](/en/blog/best-electronic-invoicing-software/).

The challenge for end users is less to know the exact syntax than to verify that their software or PDP covers the three formats in input and output. A good practice consists of requesting a certificate of EN 16931 compliance and a test journal with a sample of invoices issued and received in each of the three syntaxes. European tax administrations recommend these verifications, and the official interoperability tests published by the DGFiP allow validating the complete chain.

## Validation, Schematron and conformance testing

Beyond syntactic respect of the schemas, an electronic invoice must satisfy a battery of business rules to be considered conformant in the regulatory sense. The EN 16931 standard incorporates a set of identified rules (BR-01 to BR-CO-25 for the core, plus extensions), each one validating a coherence between mandatory data. The most frequent rules concern the consistency of totals (sum of lines equals total excluding VAT), the presence of a VAT identifier when the operation is taxable, the validity of date formats and currency codes, and the presence of a unique identifier per invoice line.

These rules are implemented in Schematron files published by CEN, OpenPeppol and the FNFE-MPE. A Schematron file is an XSLT transformation that traverses the XML invoice and emits an error or a warning for each non-respected rule. PDPs use these Schematrons in their automatic input filter: an invoice that fails a blocking rule is rejected before being routed, with a structured error message returned to the issuer. The error message respects a normalized format (CEFACT BusinessAcknowledgement or specific rejection schema), allowing the issuing software to display it directly to the user.

The interoperability tests organized by the DGFiP and the AIFE in 2024 and 2025 made it possible to identify the most frequent rejection cases. Three categories dominate: invoice numbering (duplicates or non-respected sequences), VAT calculation errors (rounding, base inconsistency) and incorrect identifiers (SIREN/SIRET malformed, intra-EU VAT number not recognized). Software publishers have refined their integrated controls based on these findings, and the failure rate at the first transmission has fallen significantly between the early test waves and the regulatory deadlines. Continuous validation upstream of the dispatch is now considered a core function of any compliant accounting software.

## Storage, archiving and probative value

The format choice also has direct consequences on the legal archiving of invoices. French law requires conservation of invoices for ten years, with the obligation to guarantee the integrity, intelligibility and durability of the document throughout the entire conservation period. For Factur-X, the PDF/A-3 is precisely designed for long-term archiving: ISO 19005-3 incorporates self-sufficiency constraints (embedded fonts, no JavaScript, no external links) that guarantee future readability. The embedded CII XML benefits from the same protection.

For pure UBL and CII, archiving the XML alone is theoretically sufficient, since the syntax is open and the schemas are public. In practice, companies often associate a generated visualization PDF (via XSLT transformation or a viewer tool) to facilitate human consultation in case of audit. This visualization PDF has no probative value of its own, the legal reference remains the XML signed and timestamped by the PDP. Some companies choose to encapsulate the XML in a PDF/A-3 themselves to align all flows on a single Factur-X type archive format, even when the original syntax is UBL.

Electronic signature and qualified timestamping reinforce the probative value of the invoice. The PDP applies a qualified electronic signature (in the eIDAS regulation sense) to each transmitted invoice, which guarantees the integrity and authenticity of the file at the moment of dispatch. The timestamp, also qualified, fixes the legal date of issuance. These elements are stored alongside the XML in the conservation archive, with the metadata necessary to rebuild the chain of custody. A correctly registered PDP includes these functions in its base service, and the issuer does not need to deploy a parallel signature infrastructure.

## Sectoral extensions and specialized profiles

The EN 16931 standard provides for the possibility of sectoral extensions to enrich the core for specific needs. Several extensions have already been published or are under construction. The XRechnung extension, used in Germany for B2G flows, adds rules on payment references and contracting authority identifiers. The UBL Invoice for Construction extension specializes the format for the building trades, with situation lines, retention of guarantee and price revision. The Peppol BIS Billing 3.0 specification itself is an extension of EN 16931, with stricter validation rules and additional fields for international flows.

In France, no general sectoral extension has been imposed by the DGFiP at this stage, but several professional federations are working on profiles adapted to their issues. The automotive sector is studying a CII profile aligned with Odette and JAMA practices, the agri-food sector is exploring a Factur-X profile with additional traceability fields, and the temporary work sector is considering specific extensions for time tracking and assignment lines. These initiatives respect the principle of upward compatibility: an extended invoice must remain readable by a tool that only knows the core, additional fields are simply ignored or stored as is.

The EXTENDED profile of Factur-X anticipates this need by providing additional fields beyond EN 16931 for complex business cases: contractual references in cascade, multi-period payment terms, complex foreign currency information, multiple regulatory references. This profile is mainly used by large groups with detailed contractual exchanges and is sometimes required by certain key account buyers in their supplier specifications. Software publishers progressively integrate the EXTENDED profile, but the EN 16931 profile remains the default reference for the majority of B2B exchanges.

## Companion resources for context

Several adjacent topics help frame the format question within the broader reform. The [mandatory electronic invoicing](/en/blog/mandatory-electronic-invoicing/) page details the legal scope of the obligation. The [electronic invoicing timeline](/en/blog/electronic-invoicing-timeline/) recaps the deployment phases by company size, including the September 2026 milestone that activates the issuance obligation in EN 16931 syntax. For very small businesses and the self-employed, [electronic invoicing for the self-employed](/en/blog/electronic-invoicing-self-employed/) and [electronic invoicing for very small businesses](/en/blog/electronic-invoicing-very-small-business/) explain how the choice of Factur-X by default impacts very small structures. SMEs will find practical implementation logic in [electronic invoicing for SMEs](/en/blog/electronic-invoicing-sme/), where format choice and PDP selection are detailed jointly. These resources are not technical duplicates, they shed light on the format question from the angle of business size and operational priorities.

## Frequently asked questions

<details>
<summary>What are the three electronic invoice formats accepted in France from September 2026?</summary>

The reform stemming from decree 2022-1299 and the order of 22 June 2023 retains three mandatory syntaxes for the interoperability core: Factur-X, UBL and CII. All three must comply with the semantic reference of the European EN 16931 standard published by CEN. The PPF (Public Invoicing Portal) and every registered PDP (Partner Dematerialization Platform) must issue, receive and convert these three formats. Proprietary EDI flows remain marginally accepted between PDPs, but the translation to one of the three standardized formats remains mandatory at output.
</details>

<details>
<summary>What is the difference between Factur-X and ZUGFeRD?</summary>

Factur-X and ZUGFeRD are two names for the same hybrid format, jointly developed by the Forum National de la Facture Electronique (FNFE-MPE) in France and the Forum elektronische Rechnung Deutschland (FeRD) in Germany. Versions 1.0 and above are aligned and technically interoperable. The Factur-X name is used in France and the ZUGFeRD name is used in Germany, but the EN 16931, BASIC, EXTENDED and MINIMUM profiles carry the same tags and the same embedded CII XML structure inside the PDF/A-3.
</details>

<details>
<summary>Should you choose UBL, CII or Factur-X for your accounting software?</summary>

The choice depends on the context. Factur-X suits companies that want a gradual migration with human readability of the preserved PDF. UBL is favored in environments already tooled for Peppol or European e-commerce. CII remains the natural choice for large industrial groups and sectors where UN/CEFACT has historically dominated, such as automotive and large-scale retail. In any case, a properly registered PDP is required to ensure conversion between the three, so the initial choice is not locking.
</details>

<details>
<summary>Does the EN 16931 standard impose a single technical format?</summary>

No. The EN 16931 standard, published by the European Committee for Standardization, defines a common semantic model, that is, the list of mandatory invoice information (identifier, dates, seller, buyer, lines, totals, VAT, contractual references). It does not freeze the XML syntax. Two syntaxes are recognized as compliant under the standard: UBL 2.1 (CEN/TS 16931-3-2) and CII 16B (CEN/TS 16931-3-3). Factur-X reuses the CII syntax embedded in a PDF/A-3.
</details>

<details>
<summary>How does Peppol BIS Billing 3.0 fit relative to the French formats?</summary>

Peppol BIS Billing 3.0 is an implementation specification published by OpenPeppol AISBL, based on UBL 2.1 and compliant with EN 16931. It is already used as an exchange backbone by Nordic, Dutch and Belgian administrations. France does not make Peppol its official channel, but registered PDPs must guarantee interoperability with Peppol access points for inbound and outbound flows involving European partners already connected to the network.
</details>
