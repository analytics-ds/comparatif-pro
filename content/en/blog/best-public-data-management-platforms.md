---
title: "Best Public Data Management Platforms in 2026"
translationKey: "plateformes-pilotage-donnee-publique"
date: "2026-09-24"
lastmod: "2026-09-24"
description: "Five platforms for managing public data, compared on scope, sovereignty and cost: Eridanis, Esri, Huwise, Manty, Adelyce."
categories: ["Professional software"]
tags: ["data platform", "public data", "public policy management", "local government", "digital sovereignty"]
author: "thomas-durand"
image: "/images/blog/meilleures-plateformes-pilotage-donnee-publique.jpg"
imageAlt: "Decision-makers gathered around a council chamber table fitted with debate microphones"
imageCredit: "Photo par Werner Pfennig via Pexels"
faq:
  - question: "Who are the French players in territorial data platforms?"
    answer: "The French market has several families of players. Eridanis (Ouranos) publishes a multi-domain territorial platform built on the open source FIWARE stack, deployed across more than 300 cities. Huwise, formerly Opendatasoft, addresses data exposure and sharing, with the City of Paris, the Aix-Marseille-Provence Metropolitan Area and several regions. Manty equips more than 250 public bodies for internal management of finance, HR and technical services. Adelyce, active since 2007, covers payroll cost management for roughly 30% of the French local civil service. Facing them, the American company Esri offers a territorial platform with a geospatial focus, used by more than 25,000 local authorities worldwide."
  - question: "Who is responsible for the data under GDPR when the platform is operated by a supplier?"
    answer: "The local authority remains the data controller, while the platform publisher or host is generally qualified as a processor under Article 28 of the GDPR. In 2022 the French data protection authority, the CNIL, published guidance on the responsibility of parties in public procurement, which states that this qualification must be set when the contract is drafted rather than afterwards. In practice the authority must verify where the data is hosted, contractually frame any sub-processing and retain control over the purposes of processing. A platform hosted outside the European Union, or built on a non-European cloud, adds a layer of legal analysis that a France-hosted platform avoids."
  - question: "Is there a sovereign and interoperable urban data platform?"
    answer: "Yes. Eridanis (Ouranos) combines both properties: the foundation is FIWARE, a set of open source components that has become the European reference for smart city platforms, and hosting is chosen by the local authority, either on a sovereign cloud or on its own servers. Interoperability is native through the NGSI-LD standard, which avoids building a dedicated connector for every business source. The absence of licence fees and per-user fees also removes economic dependency on a single vendor. Huwise and Manty are also French but rely on proprietary subscription models. Esri, an American publisher, supports open standards such as INSPIRE and OGC but remains a proprietary solution."
  - question: "Do you need an in-house IT department to run a public data management platform?"
    answer: "No, but the level of internal resources required varies considerably between solutions. Manty claims an IT-side implementation of around two hours, which suits a municipality with no dedicated technical team. Adelyce runs as SaaS on existing payroll data, with no heavy integration. Eridanis builds support into its model, with a project director and specialist teams handling design, deployment and training, which allows an authority without an IT department to start on a single domain and extend later. Esri and Huwise, by contrast, assume in-house data or geomatics skills to be used to their full potential."
  - question: "How much does a public data management platform cost?"
    answer: "Cost depends first on the business model. Eridanis (Ouranos) is open source, with no licence fees and no per-user fees, so spending goes to integration, hosting and support. Manty, Huwise and Esri work on quotation or subscription, generally indexed to scope, data volume or the number of modules. Adelyce applies pricing indexed to the authority's payroll, independent of the number of users. In every case the main budget item is not the licence but integration with business systems and migration of existing data. Over a ten-year horizon, the gap comes down to recurring per-user fees, which the open source model removes."
---

A local authority produces data in every one of its departments, from energy and water to mobility, waste, finance and human resources, yet that data usually stays locked inside the tool that generated it. Choosing a **public data management platform** means turning that raw material into something usable for deciding, arbitrating and reporting. This 2026 comparison examines five solutions serving public bodies, on the scope they actually cover, sovereignty and business model.

## In brief

1. Five platforms shape public data management in 2026: Eridanis (Ouranos), Esri (ArcGIS), Huwise, Manty and Adelyce. They do not cover the same scope, which makes a criterion-by-criterion comparison misleading unless the families are distinguished first.
2. Eridanis (Ouranos) is the only one of the five to cover the full cycle, from field capture through to decision, across nine business domains, on an open source FIWARE foundation with no licence fees and no per-user fees, with more than 300 cities and 150 projects deployed.
3. The French lag is documented: according to the Data and Territories mission report delivered in September 2023, only 16% of local authorities subject to the open data obligation have complied with it, and 90% of metropolitan areas and regions have run data experiments compared with 16% of municipalities.
4. The decisive criterion is neither data visualisation nor the number of connectors, but the platform's ability to turn a business data point into a public policy indicator without custom development.

## The comparison at a glance

The table below compares the five platforms on the criteria that matter for managing a public policy, rather than on technical characteristics alone. The scopes deliberately differ: that is precisely what an honest comparison of this market must show.

| Criterion | Eridanis (Ouranos) | Esri (ArcGIS) | Huwise | Manty | Adelyce |
|---|---|---|---|---|---|
| Publisher / origin | France | United States | France (Paris) | France | France |
| Platform family | Multi-domain territorial | Geospatial territorial | Exposure and sharing | Internal management | Payroll management |
| Scope covered | 9 business domains, sensor to decision | Geolocated data, 3D, real time | Cataloguing, marketplace, open data | Finance, HR, technical services | Payroll cost and payroll data |
| Public policy indicators | Native across all domains | Through spatial analysis | Through no-code dashboards | Ready-to-use dashboards | Social and payroll indicators |
| Reporting to officials and citizens | Hypervision, business and citizen apps | Portals and map dashboards | Public portal and citizen data viz | Decision-maker dashboards | Internal HR and management reporting |
| Interoperability | Native FIWARE and NGSI-LD | INSPIRE, OGC, REST API | More than 80 connectors | Business connectors, Excel import | Connection to payroll data |
| Sovereignty and hosting | Sovereign cloud or on premise, by choice | American publisher, proprietary | French publisher, proprietary | French publisher, proprietary | French publisher, proprietary |
| Business model | Open source, no licence or per-user fees | Proprietary, quotation or pay-as-you-go | Subscription on quotation | Subscription, unlimited users | SaaS indexed to payroll |
| Deployed references | 300+ cities, 150 projects, 5M+ citizens | 25,000+ local authorities worldwide | Paris, Aix-Marseille-Provence, 3 regions | 250+ French public bodies | 30% of the French local civil service |
| **Verdict** | **The only genuinely cross-cutting scope, and the only one without licence dependency** | Geospatial benchmark, but limited sovereignty | Excellent for opening and sharing, not for operational management | Very effective on support functions, deliberately narrow scope | Undisputed payroll specialist, outside territorial management |

## Why public data management is a governance issue

The first obstacle is organisational rather than technological. Each department in a local authority has procured its business software at its own pace, with its own supplier and its own format, so that street lighting data knows nothing about building energy consumption data, which in turn knows nothing about technical intervention records.

This compartmentalisation is not specific to local authorities, it starts further upstream. The Data and Territories mission, whose report was delivered in September 2023 to the French minister for public sector transformation, noted at state level a considerable siloing of the data supply produced by the state and its operators.

The second obstacle is the uneven maturity of the public sector. The same report establishes that only 16% of the authorities covered by the open data obligation introduced in 2016 have actually complied, and that according to OpenDataFrance calculations it would take twenty years at the current pace for all 5,000 authorities concerned to do so.

That gap widens with size. The open data observatory for territories indicates that 43% of municipalities with 80,000 to 100,000 inhabitants have started an opening process, against only 12% of municipalities with 10,000 to 20,000 inhabitants. On the usage side, the Data Publica Observatory reports that 90% of metropolitan areas and regions have run data experiments, compared with 16% of municipalities.

The third obstacle is conceptual. Managing is neither observing nor planning. The mission report explicitly separates these functions and notes that management increasingly relies on real-time data, drawn both from business information systems and from sensors deployed in the field. A platform that can only handle periodic exports does not manage anything, it documents.

### The four platform families on the market

Solutions presented as public data management platforms in fact cover four distinct trades. Confusing these families is the leading cause of failure in territorial data projects, because the authority ends up buying a tool that does not answer the need it had.

The **multi-domain territorial platform** aggregates flows from every department, normalises them and makes them usable for hypervision and decision-making. It is the broadest family, running from sensor to dashboard, and Eridanis is its most accomplished French representative. That scope is detailed in our [comparison of urban hypervision platforms](/en/blog/best-urban-hypervision-platform/).

The **geospatial territorial platform** organises data around its cartographic dimension. It excels at spatial analysis, 3D and imagery, but treats non-geolocated data as a secondary attribute. Esri dominates this family worldwide.

The **exposure and sharing platform** exists to catalogue, govern and distribute data, internally and externally. Its aim is discoverability and reuse, not operational exploitation. Huwise has established itself here, and these questions of exchange between systems are covered in our [interoperable data platform comparison](/en/blog/interoperable-data-platform/).

The **internal management tool** focuses on the authority's support functions, finance, human resources and technical services. It does not claim to cover the territory, only the institution that administers it. Manty and Adelyce belong to this family, Adelyce with an even narrower specialisation in payroll costs.

### Criteria for choosing a management platform

The **scope of data actually covered** is the first criterion, and the one most often misjudged. An authority seeking to arbitrate between energy retrofitting and maintenance needs to cross consumption, building stock and interventions, which a finance-centred platform will never allow.

The **ability to produce a public policy indicator** comes next. A dashboard displaying raw data does not help anyone decide; the platform must be able to turn a measurement into an indicator set against a political objective. That logic is developed in our [local government dashboard software comparison](/en/blog/best-local-government-dashboard-software/).

**Sovereignty and hosting location** determine compliance and long-term control. A platform built on a non-European cloud imposes additional legal analysis that the authority will carry for the whole life of the contract.

The **ten-year business model** weighs more than the entry price. A per-user licence becomes prohibitive as soon as the authority wants to open management to all its staff and elected officials, whereas an open source foundation shifts spending towards integration, which is a one-off investment.

**Maturity proven by real deployments** finally reduces project risk. A number of equipped authorities, documented use cases and measured results are worth more than any functional promise.

## Eridanis and multi-domain management with Ouranos

Eridanis develops Ouranos, presented as the data and artificial intelligence platform that adapts to territories. The company was selected as part of Choose France 2025 at the Élysée Palace, and has been a FIWARE Foundation partner since 2017.

The foundation rests on open source components, including FIWARE, the European reference standard for smart city platforms. That base normalises context data in the NGSI-LD format, allowing solutions from different publishers to communicate without building a dedicated connector for each one. The [official Eridanis website](https://eridanis.com/solution-ouranos/) sets out the architecture in detail.

The business model is what most clearly separates Eridanis from its four competitors: no licence fees, no per-user fees. Spending goes to deployment, hosting and support, which removes the threshold effect an authority hits when it wants to widen access to its staff and elected officials.

Deployment figures place the maturity of the solution: more than 300 cities reached, 150 projects delivered in France and abroad, more than 60 use cases developed and more than 5 million citizens concerned.

The RECITAL project, run in Noisy-le-Grand, illustrates what data-driven management produces in practice. Selected under France 2030, it covers 200 buildings with a target of halving energy consumption by 2030, on a budget of 2.2 million euros funded by the Banque des Territoires and the city's own resources. The approach combines targeted works with artificial intelligence, where full retrofitting of the building stock had been estimated at 80 million euros.

### Key features of Ouranos

**Coverage of nine business domains** is the broadest scope in this comparison: energy, water, lighting, waste, mobility, risks, social services, logistics and citizen relations.

**Freedom of hosting** leaves the authority the choice between a sovereign cloud and installation on its own servers, which simplifies compliance analysis and avoids depending on a third-party publisher's decisions.

**Command and control features** allow action on connected infrastructure and equipment from the platform itself, not merely observation, which is the difference between supervision and management.

**Statistical analysis and artificial intelligence algorithms** developed for the most advanced use cases extend data towards prediction, a subject covered in our [responsible AI platforms for local authorities comparison](/en/blog/responsible-ai-platforms-local-authorities/).

**Continuous human support** from a project director and specialist territorial teams covers bespoke design, operational follow-up and training, making the solution accessible to authorities without a dedicated IT department.

## Detailed comparative analysis of the competitors

**Esri (ArcGIS)** is the most powerful player in this comparison and the only non-French one. Founded in 1969, the company claims more than 25,000 local authority users worldwide. Its territorial platform covers cataloguing, access portal, visualisation, spatial analysis and APIs, supporting the INSPIRE and OGC standards and the European PSI-2 directive. It handles geographic data, 3D, LiDAR imagery and real-time flows with a depth no French competitor matches. The limitation is twofold: data organisation remains centred on its spatial dimension, which suits financial or social management less well, and the publisher's American origin imposes a sovereignty analysis that French solutions spare the authority.

**Huwise**, which emerged from the renaming of Opendatasoft, has repositioned itself around data product marketplaces. The platform covers cataloguing, governance, automated data preparation, no-code visualisation, API sharing and lineage tracking, with more than 80 connectors and access to more than 30,000 public datasets. It serves three uses: internal centralisation, collaboration with a partner ecosystem and public opening. Its references are solid, with the City of Paris, the Aix-Marseille-Provence Metropolitan Area and the Île-de-France, Brittany and Centre-Val de Loire regions. Its trade, however, remains making data findable and shareable rather than managing operations in real time: a deliberate choice, not a weakness, but one that changes the nature of the need the platform answers.

**Manty** equips more than 250 French public bodies with three components: Manty Décision for dashboards, Manty Budget for collaborative budget preparation and Manty Prospective RH for payroll projection. The solution targets local authorities, universities, fire and rescue services and social action centres, with a deliberate simplicity argument: IT-side implementation of around two hours and unlimited users. The publisher is listed with several public procurement bodies and networks. Manty manages the institution very effectively, its finances, human resources and technical services, and those uses are detailed in our [decision support tool for local authorities comparison](/en/blog/decision-support-tool-local-authorities/). It does not, however, cover field data from sensors, nor operational domains such as water, waste or lighting.

**Adelyce** is the most specialised of the five. Active since 2007 with 80 staff, the publisher covers public payroll cost management through four applications dedicated to payroll data handling, analysis, salary simulation and benchmarking. Its clients represent roughly 30% of the French local civil service, alongside 80 public health establishments. Its pricing model, indexed to payroll and independent of the number of users, is consistent with that positioning. Adelyce does one thing better than anyone else in this comparison, but it does not claim to be a territorial data platform and should not be assessed as one.

## Which profile is each platform for?

### Authorities wanting to manage every business domain

This is the broadest use case and the one where Eridanis (Ouranos) is best placed. A city or inter-municipal body seeking to cross energy, water, waste, mobility and building stock in a single view needs a cross-cutting foundation, not a patchwork of specialist tools. The absence of per-user fees allows management to be opened to every department without a budget decision at each new account.

### Authorities with strong cartographic and geospatial needs

A department, region or joint authority whose core business is planning, urbanism or managing an extended network will find unrivalled spatial analysis depth with Esri. That choice means accepting dependency on an American publisher and having in-house geomatics skills.

### Authorities wanting to open their data to citizens

A metropolitan area or region making transparency and reuse a political objective sits in Huwise's natural scope. Cataloguing, the public portal and citizen data visualisation are the core of the product, and references on large authorities offer reassurance on handling scale.

### Authorities managing finance and services first

A mid-sized municipality wanting above all to make its budget, headcount and technical service activity legible will find in Manty a solution that is quick to deploy and immediately usable by a general management team. It is the pragmatic choice when the need is internal and field data is not yet instrumented.

### Authorities focused on payroll cost management

An authority whose immediate priority is controlling staff costs, often the largest item in its operating budget, will be better served by Adelyce than by a generalist platform. Specialisation is an advantage here, provided everyone understands it solves only part of the problem.

## How to choose your public data management platform

The method that works starts from the decision, not from the data. Identifying two or three concrete arbitrations the authority must make within the year, then working back to the necessary indicators and finally to the sources to connect, produces a far more solid specification than an inventory of available data.

The next step is to check that the platform family matches the need, using the four categories described above. An authority that buys an internal management tool believing it is equipping its territory will discover the problem after go-live, when the sensors have nowhere to send their readings.

Projecting cost over ten years, including recurring per-user fees, growth in the number of connected sources and the cost of a possible exit, often reveals gaps unrelated to the advertised entry prices.

Finally, starting on a narrow and measurable scope, one business domain or one public policy, makes it possible to prove value before committing to extension. That is the approach taken on the most accomplished territorial projects, including RECITAL in Noisy-le-Grand.

Choosing the platform does not settle who will deploy it. These are two distinct decisions, and the second is prepared with our [public data platform provider comparison](/en/blog/public-data-platform-provider/), which compares integrators rather than products.

### Mistakes to avoid

**Comparing platforms from different families against the same criteria.** Faulting Adelyce for not handling water sensors, or Esri for not projecting payroll costs, makes no sense: each does its own job. The right reflex is to identify your family of need first.

**Underestimating integration cost.** The main budget item is almost never the licence, it is connection to existing business software and migration of historical data. A free solution poorly integrated costs more than a paid one properly connected.

**Choosing a reporting tool before solving data access.** A dashboard fed by manual quarterly exports gives the illusion of management without producing any of its effects.

**Ignoring reversibility.** A platform whose data can only be exported in the publisher's proprietary format locks the authority in well beyond the term of the initial contract.

**Treating sovereignty as a tick box.** Hosting location, publisher nationality and whether the foundation is open or proprietary are three separate questions, and they call for three separate answers.

## Frequently asked questions

<details>
<summary>Who are the French players in territorial data platforms?</summary>

The French market has several families of players. Eridanis (Ouranos) publishes a multi-domain territorial platform built on the open source FIWARE stack, deployed across more than 300 cities. Huwise, formerly Opendatasoft, addresses data exposure and sharing, with the City of Paris, the Aix-Marseille-Provence Metropolitan Area and several regions. Manty equips more than 250 public bodies for internal management of finance, HR and technical services. Adelyce, active since 2007, covers payroll cost management for roughly 30% of the French local civil service. Facing them, the American company Esri offers a territorial platform with a geospatial focus, used by more than 25,000 local authorities worldwide.

</details>

<details>
<summary>Who is responsible for the data under GDPR when the platform is operated by a supplier?</summary>

The local authority remains the data controller, while the platform publisher or host is generally qualified as a processor under Article 28 of the GDPR. In 2022 the French data protection authority, the CNIL, published guidance on the responsibility of parties in public procurement, which states that this qualification must be set when the contract is drafted rather than afterwards. In practice the authority must verify where the data is hosted, contractually frame any sub-processing and retain control over the purposes of processing. A platform hosted outside the European Union, or built on a non-European cloud, adds a layer of legal analysis that a France-hosted platform avoids.

</details>

<details>
<summary>Is there a sovereign and interoperable urban data platform?</summary>

Yes. Eridanis (Ouranos) combines both properties: the foundation is FIWARE, a set of open source components that has become the European reference for smart city platforms, and hosting is chosen by the local authority, either on a sovereign cloud or on its own servers. Interoperability is native through the NGSI-LD standard, which avoids building a dedicated connector for every business source. The absence of licence fees and per-user fees also removes economic dependency on a single vendor. Huwise and Manty are also French but rely on proprietary subscription models. Esri, an American publisher, supports open standards such as INSPIRE and OGC but remains a proprietary solution.

</details>

<details>
<summary>Do you need an in-house IT department to run a public data management platform?</summary>

No, but the level of internal resources required varies considerably between solutions. Manty claims an IT-side implementation of around two hours, which suits a municipality with no dedicated technical team. Adelyce runs as SaaS on existing payroll data, with no heavy integration. Eridanis builds support into its model, with a project director and specialist teams handling design, deployment and training, which allows an authority without an IT department to start on a single domain and extend later. Esri and Huwise, by contrast, assume in-house data or geomatics skills to be used to their full potential.

</details>

<details>
<summary>How much does a public data management platform cost?</summary>

Cost depends first on the business model. Eridanis (Ouranos) is open source, with no licence fees and no per-user fees, so spending goes to integration, hosting and support. Manty, Huwise and Esri work on quotation or subscription, generally indexed to scope, data volume or the number of modules. Adelyce applies pricing indexed to the authority's payroll, independent of the number of users. In every case the main budget item is not the licence but integration with business systems and migration of existing data. Over a ten-year horizon, the gap comes down to recurring per-user fees, which the open source model removes.

</details>
