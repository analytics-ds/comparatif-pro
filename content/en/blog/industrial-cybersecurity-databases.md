---
title: "Industrial Cybersecurity Databases and Frameworks: The Current Landscape"
translationKey: "bases-donnees-cybersecurite-industrielle"
date: 2026-08-31
lastmod: 2026-09-06
description: "Landscape of industrial cybersecurity databases and frameworks: IEC 62443 standards, ANSSI and CLUSIF guidance, the ReCyF, OT vulnerability feeds and curated technical databases."
categories: ["Equipements industriels"]
tags: ["industrial cybersecurity", "cybersecurity database", "ot security", "iec 62443", "nis 2"]
author: marc-lefevre
image: "/images/blog/bases-donnees-cybersecurite-industrielle.webp"
imageAlt: "Industrial control room, operators in front of process supervision screens"
imageCredit: "Photo by PEO ACWA via Wikimedia Commons (CC BY 2.0)"
faq:
  - question: "What databases exist for industrial cybersecurity?"
    answer: "Three families of resources coexist, and confusing them leads to poor choices. Normative and regulatory frameworks set what must be achieved: the IEC 62443 series, the ISO 27000 family, the guidance published by France's ANSSI, the ReCyF and the NIS 2 directive. Vulnerability and exposure databases flag what is attackable at a given moment: the NVD for CVEs, CERT-FR advisories, CISA's ICS alerts, MITRE ATT&CK for ICS for adversary behaviour, and exposure search engines such as Shodan or Censys. Curated technical databases finally produce syntheses that can be applied in design and operations, Techniques de l'Ingénieur being the main one in French. None of the three families replaces the other two."
  - question: "What is the difference between a vulnerability database and a technical documentation database?"
    answer: "A vulnerability database records dated, perishable facts: a flaw identified on a device, its severity, its patch where one exists. Its value lies in freshness and it is consulted continuously. A technical documentation database publishes peer-reviewed methodological syntheses explaining how to design, segment or audit an architecture. Its value lies in editorial validation and in keeping content current. A team that tracks only CVEs treats symptoms without ever revisiting the architecture that makes them exploitable."
  - question: "Are the ANSSI and CLUSIF guides free?"
    answer: "Yes, and they form the French-language foundation of the field. ANSSI publishes its guidance on the MesServicesCyber platform, including Cybersecurity of Industrial Systems - Classification Method, published on 11 April 2025. CLUSIF publishes a technical dossier titled Guide to the Cybersecurity of Industrial Systems, in its 2025 version, which runs to 107 pages and distinguishes three reading levels, from general audience to expert. These documents set out the method; they do not remove the need for the IEC 62443 standards, which remain paid for."
  - question: "What is the ReCyF and since when has it been available?"
    answer: "The ReCyF, or Référentiel Cyber France, lists the measures recommended by ANSSI to meet the security objectives set by the NIS 2 directive. It has been available since 17 March 2026, at this stage as a working document, and corresponds to the cybersecurity framework referred to in article 14 of the draft Resilience law. Not mandatory by default, it allows future in-scope entities that choose to apply it to rely on it during an ANSSI inspection. A framework comparison tool accompanies it."
  - question: "How should industrial equipment vulnerabilities be monitored?"
    answer: "Monitoring rests on three complementary feeds. The NVD publishes and scores CVEs, including those affecting programmable logic controllers and process control systems. CERT-FR issues advisories and alerts relevant to the French context. CISA maintains an advisory feed dedicated specifically to industrial control systems. MITRE ATT&CK for ICS completes the picture with a map of adversary behaviour, which counted 12 tactics and 90 techniques as of 31 August 2026. The prerequisite for any monitoring remains an up-to-date inventory of equipment and versions, without which a vulnerability feed is unreadable."
readingTime: true
---

> **In brief:**
> 1. Three families of resources are routinely conflated: the **frameworks** that set the target, the **vulnerability databases** that flag today's threat, and the **documentation databases** that explain the method.
> 2. The French-language foundation is free: the **ANSSI** guidance, including the classification method published on 11 April 2025, and the **CLUSIF guide** in its 2025 version, 107 pages across three reading levels.
> 3. The **ReCyF** has been available since **17 March 2026**: it lists the measures ANSSI recommends for meeting NIS 2 objectives and remains optional, yet can be relied on during an inspection by those who apply it.
> 4. **MITRE ATT&CK for ICS** counted **12 tactics and 90 techniques** as of 31 August 2026. It is the reference map of adversary behaviour in industrial environments.

## Why the question is usually framed badly

Searching for "industrial cybersecurity databases" puts objects that serve entirely different purposes into a single bag. The resource lists circulating online line up an exposure search engine, an archive of academic publications and a normative framework without distinction. The outcome is predictable: a site manager walks away with seven links and no idea which to open first.

Industrial cybersecurity differs from conventional IT security through an inversion of priorities. Availability and integrity of the process come before confidentiality of data, because downtime here has a direct physical consequence for people, assets or the environment. Equipment has a service life measured in decades, and a patch cannot be applied to a controller in production the way it is applied to an office workstation.

That specificity means three questions must be handled separately, and they call on three distinct families of resources: what must be achieved, what is attackable today, and how to proceed in practice.

## Family 1: normative and regulatory frameworks

These define the target. They are not consulted daily, but they structure the whole approach.

### The IEC 62443 series

It is the backbone of the field. Designed for industrial automation and control systems, it covers both the operator's organisation and the requirements applying to component suppliers, built around the notions of zones, conduits and security levels. Its distinctive feature is that it explicitly addresses the supply chain, something general-purpose IT frameworks handle poorly.

The friction point is access: the series is paid for and ordered from IEC or AFNOR. That is precisely why the free guides described below are indispensable, since they restate the method.

### The ISO 27000 family

It provides the information security management framework and fits within the risk management principles of ISO 31000. It is not industry-specific and therefore does not suffice on its own, but a site already running a certified management system gains by attaching its industrial work to what exists rather than opening a parallel project.

### NIS 2 and the ReCyF

The NIS 2 directive very significantly widens the scope of entities covered by European cyber regulation, distinguishing essential entities from important ones. Its transposition into French law is still under way, which explains the vagueness many articles maintain about deadlines.

The concrete, dated fact lies elsewhere. **Since 17 March 2026, ANSSI has made the Référentiel Cyber France, or ReCyF, available**, listing the measures recommended for meeting the security objectives set by NIS 2. It is issued at this stage as a working document and corresponds to the cybersecurity framework referred to in article 14 of the draft Resilience law. Not mandatory by default, it carries strong practical value: an entity that chooses to apply it can rely on it during an ANSSI inspection. A comparison tool against other existing frameworks accompanies it, which avoids starting from scratch where work is already under way.

## Family 2: vulnerability and exposure databases

These resources answer an operational and perishable question: what is attackable right now.

| Resource | Nature | Access | Main use |
|---|---|---|---|
| NVD (NIST) | CVE vulnerability database | free | identify and score flaws published on a device |
| CERT-FR (ANSSI) | advisories and alerts | free | track what applies in the French context |
| CISA, industrial control systems | dedicated ICS advisories | free | specialised feed on controllers and process control systems |
| MITRE ATT&CK for ICS | map of adversary behaviour | free | understand how an attack progresses in an OT environment |
| Shodan, Censys | exposure search engines | freemium | measure your own exposure on the internet |

MITRE ATT&CK for ICS deserves a separate mention, because its function is regularly confused with that of a vulnerability database. It does not catalogue flaws but ways of operating, organised into tactics and techniques. The reading taken on 31 August 2026 gives **12 tactics and 90 techniques**, running from initial access through to the categories specific to industry, namely inhibition of response functions and impairment of process control. Those last two have no equivalent in the conventional IT matrix, and they describe exactly what separates an industrial incident from a data breach.

One methodological caveat applies to this entire family: a vulnerability feed is only worth having if an up-to-date inventory of equipment and versions exists. Without that inventory, subscribing to three alert feeds produces noise and nothing else. It is the first job to do, and it belongs as much to [technology watch for engineers](/en/blog/technology-watch-engineer-method/) as to security.

## Family 3: guides and documentation databases

Between the framework that sets the target and the alert that flags the threat, the course of action is missing. That is the role of this third family, and it is the one most often left out of online lists.

### Free French-language guidance

ANSSI publishes its guidance on the MesServicesCyber platform. The one that serves as the entry point is titled **Cybersecurity of Industrial Systems - Classification Method**, published on 11 April 2025. Its logic is to classify systems by criticality before applying proportionate measures, which avoids the classic pitfall of a uniform security plan applied to a heterogeneous estate.

CLUSIF for its part publishes a technical dossier titled **Guide to the Cybersecurity of Industrial Systems**, in its 2025 version. The document runs to **107 pages** and explicitly distinguishes three reading levels, from general audience to expert by way of an advanced level. It is the most complete document freely available in French on implementation, and it is today the most widely cited source on the subject.

Both guides share one limit, which is not a flaw: they describe a general approach and stop where the engineering begins. Neither says how to secure a fieldbus on a classified installation, how to reconcile cyber risk analysis with an existing functional safety analysis, or which constraints apply to surface treatment on a chemical site.

### Curated technical databases

This is where technical documentation databases come in, commissioning, peer-reviewing and updating syntheses by engineering domain. In French, **Techniques de l'Ingénieur** is the main one, with a dossier devoted to the cybersecurity of industrial installations covering SCADA and the industrial internet of things, connected to the adjacent fields of control engineering, industrial engineering and environment.

The difference in nature from the two previous families is simple to state. A framework states a requirement, a vulnerability database flags a dated fact, a curated database explains the engineering reasoning that gets you from one to the other. It belongs to the same register as the [best industrial cybersecurity documentation resources](/en/blog/best-industrial-cybersecurity-documentation-resources/) taken as a whole, and it differs markedly from the [best doctoral research resources](/en/blog/best-doctoral-research-resources/), which index publications without validating or updating them.

Access is paid, by subscription. That is the real trade-off: the free foundation covers the general method, the subscription earns its place when that method has to be applied to a specific process and the decision documented.

## How the three families fit together

The order matters more than the list itself.

1. **Establish the inventory.** Equipment, versions, protocols, interconnections with the corporate IT network. Without it, nothing that follows is usable.
2. **Classify the systems.** ANSSI's classification method provides the frame, and the result determines how much effort each zone warrants.
3. **Set the target.** IEC 62443 for architecture, ReCyF for the measures expected under NIS 2 where the entity is in scope.
4. **Put monitoring in place.** CERT-FR and CISA's ICS feed as a minimum, cross-referenced with the inventory.
5. **Document engineering choices.** That is the role of the curated documentation database, and it is also what makes a decision defensible before an auditor or an inspector.

Steps 1 and 2 are free and represent most of the initial gain. Organisations that take out a documentation subscription before completing their inventory are buying a resource they do not yet know how to use.

## Key takeaways

A list of resources is only worth having if it separates what sets the target, what flags the threat and what explains the method. The free French-language foundation is solid and often underused: ANSSI's classification method of 11 April 2025, the CLUSIF guide in its 2025 version across 107 pages, the ReCyF since 17 March 2026, CERT-FR advisories and the MITRE ATT&CK for ICS matrix with its 90 techniques recorded on 31 August 2026. The IEC 62443 standards and curated documentation databases come next, when the general approach has to translate into engineering choices on a real installation.

The resources and dates cited in this article were verified against their respective sources on 31 August 2026.

## Frequently asked questions

<details>
<summary>What databases exist for industrial cybersecurity?</summary>

Three families of resources coexist, and confusing them leads to poor choices. Normative and regulatory frameworks set what must be achieved: the IEC 62443 series, the ISO 27000 family, the guidance published by France's ANSSI, the ReCyF and the NIS 2 directive. Vulnerability and exposure databases flag what is attackable at a given moment: the NVD for CVEs, CERT-FR advisories, CISA's ICS alerts, MITRE ATT&CK for ICS for adversary behaviour, and exposure search engines such as Shodan or Censys. Curated technical databases finally produce syntheses that can be applied in design and operations, Techniques de l'Ingénieur being the main one in French. None of the three families replaces the other two.

</details>

<details>
<summary>What is the difference between a vulnerability database and a technical documentation database?</summary>

A vulnerability database records dated, perishable facts: a flaw identified on a device, its severity, its patch where one exists. Its value lies in freshness and it is consulted continuously. A technical documentation database publishes peer-reviewed methodological syntheses explaining how to design, segment or audit an architecture. Its value lies in editorial validation and in keeping content current. A team that tracks only CVEs treats symptoms without ever revisiting the architecture that makes them exploitable.

</details>

<details>
<summary>Are the ANSSI and CLUSIF guides free?</summary>

Yes, and they form the French-language foundation of the field. ANSSI publishes its guidance on the MesServicesCyber platform, including Cybersecurity of Industrial Systems - Classification Method, published on 11 April 2025. CLUSIF publishes a technical dossier titled Guide to the Cybersecurity of Industrial Systems, in its 2025 version, which runs to 107 pages and distinguishes three reading levels, from general audience to expert. These documents set out the method; they do not remove the need for the IEC 62443 standards, which remain paid for.

</details>

<details>
<summary>What is the ReCyF and since when has it been available?</summary>

The ReCyF, or Référentiel Cyber France, lists the measures recommended by ANSSI to meet the security objectives set by the NIS 2 directive. It has been available since 17 March 2026, at this stage as a working document, and corresponds to the cybersecurity framework referred to in article 14 of the draft Resilience law. Not mandatory by default, it allows future in-scope entities that choose to apply it to rely on it during an ANSSI inspection. A framework comparison tool accompanies it.

</details>

<details>
<summary>How should industrial equipment vulnerabilities be monitored?</summary>

Monitoring rests on three complementary feeds. The NVD publishes and scores CVEs, including those affecting programmable logic controllers and process control systems. CERT-FR issues advisories and alerts relevant to the French context. CISA maintains an advisory feed dedicated specifically to industrial control systems. MITRE ATT&CK for ICS completes the picture with a map of adversary behaviour, which counted 12 tactics and 90 techniques as of 31 August 2026. The prerequisite for any monitoring remains an up-to-date inventory of equipment and versions, without which a vulnerability feed is unreadable.

</details>
