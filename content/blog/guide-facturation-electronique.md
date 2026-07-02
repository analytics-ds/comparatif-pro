---
title: "Facturation electronique en France : le guide complet 2026"
description: "Guide complet de la facturation electronique en France : reforme, calendrier 2026-2027, PPF, PDP, formats Factur-X, UBL, CII, e-reporting, sanctions."
date: 2026-05-07
lastmod: 2026-05-07
publishDate: 2026-05-07
draft: false
categories: ["Services aux entreprises"]
tags: ["facturation-electronique", "reforme-2026", "tpe", "pme", "dgfip", "factur-x", "pdp"]
translationKey: "guide-facturation-electronique"
author: aurelie-vasseur
image: "/images/blog/guide-facturation-electronique.jpg"
imageAlt: "Schéma de la facturation electronique en France et de son ecosysteme reglementaire"
imageCredit: "Image issue d'Openverse (CC BY)"
faq:
  - question: "Qu'est-ce que la facturation electronique en 2026 ?"
    answer: "Il s'agit d'un dispositif obligatoire institue par l'ordonnance n° 2021-1190 du 15 septembre 2021 et le decret n° 2022-1299 du 7 octobre 2022. Toute facture entre assujettis a la TVA etablis en France doit etre transmise sous format structure (Factur-X, UBL ou CII conformes a la norme EN 16931) via le Portail Public de Facturation ou une plateforme de dematerialisation partenaire. Le dispositif s'accompagne d'une obligation de transmission de donnees (e-reporting) pour les operations B2C et internationales."
  - question: "Quelles sont les dates cles du calendrier 2026-2027 ?"
    answer: "Le 1er septembre 2026, toutes les entreprises etablies en France doivent etre capables de recevoir des factures dematerialisees. A la meme date, les grandes entreprises et les ETI sont tenues d'emettre leurs factures au format structure et de transmettre leurs donnees de e-reporting. Le 1er septembre 2027, l'obligation d'emission est etendue aux PME et aux microentreprises (TPE, auto-entrepreneurs)."
  - question: "Qu'est-ce qu'une PDP et faut-il en choisir une ?"
    answer: "Une plateforme de dematerialisation partenaire est un operateur prive immatricule par la DGFiP. Elle assure la transmission des factures structurees et des donnees de e-reporting entre assujettis et vers l'administration fiscale. Le recours a une PDP n'est pas obligatoire, le Portail Public de Facturation reste accessible gratuitement, mais une PDP apporte des services additionnels (connecteurs ERP, archivage probatoire, gestion des cycles d'approbation, formats EDI proprietaires)."
  - question: "Quels formats sont autorises ?"
    answer: "Trois formats socles sont retenus : Factur-X (PDF/A-3 avec donnees XML embarquees), UBL 2.1 (Universal Business Language) et UN/CEFACT CII (Cross Industry Invoice). Tous trois respectent la norme europeenne EN 16931. Une PDP peut convertir un format proprietaire EDI vers l'un de ces trois socles avant transmission."
  - question: "Quelles sont les sanctions en cas de non-conformite ?"
    answer: "Le Code general des impots prevoit, a l'article 1737, une amende de 15 euros par facture non conforme dans la limite de 15 000 euros par annee civile pour le defaut d'emission au format electronique. L'absence de transmission des donnees de e-reporting est sanctionnee par une amende de 250 euros par transmission omise, plafonnee a 45 000 euros par an. Au-dela des sanctions financieres, l'entreprise s'expose a un risque de redressement TVA."
---

La generalisation de la facturation electronique transforme en profondeur la relation entre les entreprises francaises et l'administration fiscale. Adoptee par l'ordonnance n° 2021-1190 du 15 septembre 2021 puis precisee par le decret n° 2022-1299 du 7 octobre 2022, la reforme institue une transmission structuree, normalisee et tracee de chaque document commercial entre assujettis a la TVA. Ce guide complet 2026 detaille le cadre legal, le calendrier officiel, les acteurs, les formats et les modalites concretes de mise en conformite.

> **En bref :**
> 1. La reforme repose sur deux piliers, l'emission obligatoire de factures dematerialisees au format structure entre assujettis francais, et la transmission de donnees fiscales (e-reporting) pour les operations B2C, B2BIE et certains paiements de services.
> 2. Calendrier officiel confirme par la loi de finances 2024 (article 91) : reception generalisee au 1er septembre 2026, emission progressive du 1er septembre 2026 (grandes entreprises, ETI) au 1er septembre 2027 (PME, TPE, microentreprises).
> 3. Trois formats socles sont reconnus : Factur-X (PDF + XML), UBL 2.1 et UN/CEFACT CII, tous alignes sur la norme europeenne EN 16931.
> 4. Le defaut de conformite expose a une amende de 15 euros par document, plafonnee a 15 000 euros par an, sans prejudice du risque de redressement TVA.

## Definition et perimetre de la facturation electronique

La facturation electronique designe l'emission, la transmission et la reception des factures sous une forme exclusivement numerique, dans un format structure ou semi-structure permettant un traitement automatise. La directive europeenne 2014/55/UE puis la norme **EN 16931** publiee par le Comite europeen de normalisation (CEN) ont pose les bases techniques d'une interoperabilite entre les systemes d'information des entreprises europeennes. La France transpose ce socle au sein de son droit interne via l'article 289 bis du Code general des impots, introduit par la loi de finances pour 2020 puis reecrit a la suite de l'ordonnance de 2021.

Le perimetre concerne l'ensemble des operations realisees entre deux assujettis a la TVA etablis en France (operations dites domestiques B2B). Les ventes a destination des consommateurs finaux (B2C), les operations transfrontalieres (B2BIE pour Business to Business International and Extracommunity) et les acquisitions intracommunautaires demeurent hors champ de l'emission obligatoire, mais restent visees par le mecanisme complementaire de transmission de donnees, le e-reporting.

Pour aller plus loin sur les obligations precises selon le statut de l'entreprise, consulter le [guide complet de l'obligation de facturation electronique](/blog/facturation-electronique-obligatoire/).

## Contexte legal et historique de la reforme

La reforme s'inscrit dans un mouvement europeen plus large de lutte contre la fraude a la TVA et de modernisation administrative. L'estimation du manque a gagner annuel pour les finances publiques francaises, le **VAT gap**, atteignait pres de 13 milliards d'euros en 2020 selon les donnees de la Commission europeenne. La transmission automatisee, en temps quasi reel, des donnees de facturation est concue comme un levier majeur pour reduire cet ecart, en s'inspirant des dispositifs deja en vigueur en Italie (**Sistema di Interscambio**, depuis 2019) ou en Espagne (**SII**).

Le calendrier initialement fixe par l'article 153 de la loi de finances pour 2020 prevoyait une mise en oeuvre entre 2024 et 2026. Un report a ete annonce par communique de presse de la Direction generale des finances publiques (DGFiP) le 28 juillet 2023, le temps de fiabiliser les briques techniques du Portail Public de Facturation. La **loi de finances pour 2024**, dans son article 91, a finalement entérine le nouveau calendrier 2026-2027.

> "Tous les assujettis a la taxe sur la valeur ajoutee etablis en France seront tenus d'accepter les factures electroniques a compter du 1er septembre 2026. L'obligation d'emission s'appliquera a la meme date pour les grandes entreprises et les entreprises de taille intermediaire, puis le 1er septembre 2027 pour les petites et moyennes entreprises et les microentreprises."
> -- Article 91 de la loi n° 2023-1322 du 29 decembre 2023 de finances pour 2024, Legifrance

L'ordonnance n° 2021-1190 du 15 septembre 2021 reste le texte fondateur. Le decret d'application n° 2022-1299 du 7 octobre 2022, complete par l'arrete du meme jour, precise les caracteristiques techniques (formats, donnees obligatoires, modalites de transmission), les conditions d'immatriculation des plateformes de dematerialisation partenaires (PDP), et les regles de gestion des statuts de cycle de vie. Le **BOFIP** publie sous la reference BOI-TVA-DECLA-30 actualise regulierement la doctrine administrative associee.

## Calendrier officiel : echeances 2026 et 2027

Le calendrier de deploiement s'echelonne en deux vagues distinctes pour l'emission, alors que l'obligation de reception est applicable simultanement a toutes les entreprises a la date butoir du 1er septembre 2026. Cette dissociation permet aux structures les plus modestes de beneficier d'une annee supplementaire pour adapter leurs outils, tout en garantissant qu'elles puissent recevoir les factures de leurs partenaires de plus grande taille des le debut.

| Echeance | Public concerne | Reception | Emission | E-reporting |
|---|---|---|---|---|
| 1er septembre 2026 | Toutes les entreprises etablies en France | Obligatoire | Selon taille (voir lignes suivantes) | Selon taille |
| 1er septembre 2026 | Grandes entreprises (plus de 5000 salaries ou plus de 1,5 milliard de chiffre d'affaires) | Obligatoire | Obligatoire | Obligatoire |
| 1er septembre 2026 | Entreprises de taille intermediaire (ETI, 250 a 4999 salaries) | Obligatoire | Obligatoire | Obligatoire |
| 1er septembre 2027 | Petites et moyennes entreprises (PME, 10 a 249 salaries) | Obligatoire (depuis 2026) | Obligatoire | Obligatoire |
| 1er septembre 2027 | Microentreprises et TPE (moins de 10 salaries) | Obligatoire (depuis 2026) | Obligatoire | Obligatoire |
| 1er septembre 2027 | Auto-entrepreneurs (regime micro-fiscal et micro-social) | Obligatoire (depuis 2026) | Obligatoire | Obligatoire |

La typologie des entreprises s'apprecie au sens du decret n° 2008-1354 du 18 decembre 2008, qui retient des seuils combinant effectifs salaries, chiffre d'affaires et total de bilan. Les details et conseils pour anticiper sont developpes dans la fiche dediee au [calendrier de la facturation electronique](/blog/calendrier-facturation-electronique/).

## Acteurs cles : DGFiP, PPF, PDP, OD et OC

L'architecture cible repose sur un schema en Y. Au centre, la **DGFiP** opere le Portail Public de Facturation et concentre les donnees de facturation a des fins fiscales. A gauche, l'emetteur depose ses factures soit directement sur le PPF, soit via une plateforme de dematerialisation partenaire (PDP). A droite, le destinataire recupere les factures via le canal de son choix.

Le **Portail Public de Facturation** (portailpro.gouv.fr), pilote par l'**Agence pour l'informatique financiere de l'Etat** (AIFE) et adosse a la plateforme Chorus Pro, joue un triple role : annuaire central des entreprises et de leurs canaux de reception, plateforme de transit gratuite pour les emetteurs n'ayant pas recours a une PDP, concentrateur des donnees a destination de l'administration fiscale.

Une **plateforme de dematerialisation partenaire** (PDP) est un operateur prive immatricule par la DGFiP au terme d'une procedure de qualification (referentiel d'exigences techniques et de securite, audit, engagement de service). Au 1er trimestre 2026, plus d'une centaine de candidats ont depose un dossier, plusieurs dizaines sont deja immatriculees a titre provisoire ou definitif. La liste officielle est tenue a jour sur le site de la DGFiP. Le choix d'une PDP repond a des criteres de couverture fonctionnelle, de robustesse et d'integration avec les systemes existants, detailles dans la fiche [plateforme de dematerialisation partenaire (PDP)](/blog/pdp-facture-electronique/).

Deux acteurs satellites completent l'ecosysteme. Les **operateurs de dematerialisation** (OD) interviennent en amont d'une PDP ou du PPF, sans transmettre directement a l'administration fiscale. Les **operateurs concentrateurs** (OC), parfois appeles tiers de confiance, agregent les flux de plusieurs entreprises avant de les remettre a une PDP. Le [role de la DGFiP dans la facturation electronique](/blog/facturation-electronique-dgfip/) decrit precisement les responsabilites respectives de chaque maillon.

## Formats acceptes : Factur-X, UBL, CII

Le decret n° 2022-1299 retient trois formats socles, tous compatibles avec la norme europeenne EN 16931. Une PDP peut accepter d'autres formats en entree (EDI proprietaire, formats sectoriels GS1 EANCOM, EDIFACT, X12) a condition de les convertir vers un des trois socles avant transmission au PPF.

| Format | Type | Specificite | Cas d'usage privilegie |
|---|---|---|---|
| Factur-X | Hybride PDF/A-3 + XML embarque | Conserve une representation visuelle PDF lisible, avec donnees structurees XML CII en piece jointe | TPE, PME, secteurs habitues au PDF, transition douce |
| UBL 2.1 | XML pur (Universal Business Language) | Standard OASIS, tres repandu en Europe du Nord et au Royaume-Uni | Echanges B2B internationaux, integration ERP avancee |
| UN/CEFACT CII | XML pur (Cross Industry Invoice) | Standard ONU, riche en donnees logistiques | Industrie, supply chain, secteurs avec donnees etendues |

Le format **Factur-X** est concu pour faciliter l'adoption par les TPE et les PME, en preservant la lecture humaine via le PDF tout en offrant une couche XML traitable par les systemes informatiques. Il s'agit d'une convergence franco-allemande avec le format **ZUGFeRD**, dont la version 2.1 est techniquement equivalente. Pour une analyse detaillee de chaque format, lire le [comparatif des formats Factur-X, UBL et CII](/blog/format-facture-electronique-factur-x-ubl-cii/).

## Entreprises concernees : du grand groupe a l'auto-entrepreneur

Le perimetre est volontairement large : toute personne assujettie a la TVA en France entre dans le champ de la reforme. Les particularites tiennent aux dates d'application differentielles selon la taille et a quelques exclusions tres ciblees (operations exonerees au sens de l'article 261 du Code general des impots, certaines operations bancaires et d'assurance).

Les **grandes entreprises** et les **ETI** sont en premiere ligne au 1er septembre 2026. Leurs systemes d'information, souvent organises autour d'un ERP central (SAP, Oracle, Microsoft Dynamics, Sage X3) et de connecteurs EDI historiques, doivent etre relies a une PDP ou au PPF, et adapter leurs cycles de validation interne (saisie, controle, approbation, comptabilisation).

Les **PME** disposent d'une annee supplementaire. Le risque pour ces structures tient surtout a la disparite des situations : certaines disposent deja d'un ERP integre, d'autres travaillent encore avec une comptabilite Excel ou un logiciel de facturation autonome. La fiche [facturation electronique des PME](/blog/facturation-electronique-pme/) detaille la methodologie de mise en conformite adaptee a ces entreprises.

Les **TPE** et les **auto-entrepreneurs** representent le segment le plus heterogene. Les editeurs de logiciels TPE (EBP, Henrri, Tiime, Indy, Pennylane, Quickbooks) ont massivement integre Factur-X dans leurs offres au cours des annees 2024-2025. Le PPF restera accessible gratuitement, ce qui permet a une microentreprise sans logiciel d'emettre ses factures via un portail web public. La fiche [facture electronique pour TPE](/blog/facture-electronique-tpe/) donne les pistes les plus economiques, et les specificites du regime micro-fiscal sont detaillees dans la fiche [facturation electronique pour auto-entrepreneur](/blog/facturation-electronique-auto-entrepreneur/).

## E-reporting : transmission de donnees pour B2C, B2BIE et paiements

A cote du flux factures B2B domestiques, la reforme instaure une obligation de transmission de donnees au profit de l'administration fiscale, le e-reporting. Trois categories de donnees sont visees, correspondant aux operations qui ne sont pas couvertes par l'emission obligatoire de factures dematerialisees.

Le **e-reporting des transactions** porte sur les ventes B2C realisees par les assujettis francais, les operations B2BIE (ventes vers ou achats depuis l'etranger), les exportations et les acquisitions intracommunautaires. Les donnees a transmettre comprennent le montant total HT, le montant de TVA par taux, la nature de l'operation, la date et le pays du client. La frequence varie selon le regime de TVA (mensuelle au reel normal, trimestrielle au reel simplifie).

Le **e-reporting des paiements** concerne les prestations de services soumises a la TVA sur les encaissements (operation au moment du paiement et non de la facturation). Il porte sur la date d'encaissement, le montant et la TVA exigible, et permet a l'administration de reconcilier la TVA exigible avec la TVA collectee declaree.

Le **e-reporting des transactions internationales B2B** cible les flux entre assujettis qui ne transitent pas par le PPF, notamment lorsqu'un fournisseur ou un client est etabli hors de France. Le mecanisme se substitue partiellement a la declaration d'echange de biens et a la declaration europeenne de services pour les flux concernes.

Toutes les donnees de e-reporting transitent par le canal d'une PDP ou du PPF, dans des formats normalises distincts des factures (schemas XML specifiques publies par la DGFiP).

## Sanctions et conformite

Le dispositif de sanctions, codifie a l'article 1737 du Code general des impots et complete par les articles 1788 D (e-reporting) et 1788 D bis (manquements aux obligations des plateformes), prevoit des amendes a la fois pour les emetteurs, les destinataires et les plateformes. La logique est graduelle : l'amende est plafonnee, mais elle s'ajoute aux sanctions de droit commun en cas de redressement TVA.

Pour l'**emetteur**, le defaut d'emission au format electronique entraine une amende de 15 euros par facture, plafonnee a 15 000 euros par annee civile. Le defaut de transmission de donnees de e-reporting expose a une amende de 250 euros par transmission omise, plafonnee a 45 000 euros par an. Pour le **destinataire**, le refus injustifie de recevoir une facture electronique conforme est sanctionne par une amende de 15 euros par facture, plafonnee a 15 000 euros par an. Pour la **PDP**, les manquements graves peuvent entrainer la suspension ou le retrait de l'immatriculation.

Au-dela des sanctions specifiques, le defaut de conformite peut entrainer un risque de remise en cause du droit a deduction de la TVA si la facture ne respecte pas les mentions obligatoires, ou si elle n'est pas archivee dans les conditions de l'article L. 102 B du Livre des procedures fiscales (six ans, support electronique inalterable).

## Conseils pratiques de mise en conformite

Une demarche de mise en conformite reussie repose sur quatre etapes structurees, dont la sequence importe autant que le contenu.

**Etape 1 : cartographier les flux de facturation.** Lister les volumes (factures clients emises, factures fournisseurs recues), distinguer les flux B2B France, B2C, B2BIE, identifier les canaux actuels (papier, PDF par mail, EDI, portail client). Cette photographie sert de base au choix d'outils.

**Etape 2 : auditer le systeme d'information.** Verifier la capacite de l'ERP ou du logiciel de facturation actuel a generer du Factur-X, de l'UBL ou du CII. Identifier les modules a faire evoluer (parametrage TVA, table des codes pays, gestion des sous-traitants, gestion des cycles d'approbation). Lister les integrations necessaires (CRM, GED, banque). Le choix d'un [logiciel de facturation electronique 2026](/blog/meilleur-logiciel-facturation-electronique/) adapte a la taille et au secteur conditionne la suite.

**Etape 3 : choisir le canal de transmission.** Le PPF gratuit suffit pour les structures les plus simples, sans volumetrie significative ni integration ERP. Une PDP devient pertinente des qu'il existe un volume significatif (plus de quelques centaines de factures par mois), des integrations comptables avancees, des besoins d'archivage probatoire ou des contraintes sectorielles (sante, BTP, distribution avec EDI). Le [comparatif des plateformes de facturation electronique](/blog/comparatif-plateformes-facturation-electronique/) detaille les criteres de selection.

**Etape 4 : tester et basculer.** Realiser une phase pilote sur un perimetre restreint (un client important, une filiale, une activite secondaire), valider le cycle complet (emission, transmission, reception, integration comptable, archivage), identifier les anomalies, puis generaliser progressivement. Il est recommande de ne pas attendre la date butoir : plus la bascule est tardive, plus le risque d'engorgement chez les editeurs et les PDP est eleve.

L'administration fiscale met a disposition une documentation evolutive sur impots.gouv.fr, des sessions de formation gratuites via les CCI et les organismes professionnels, ainsi qu'un service de support dedie pour les questions techniques liees au PPF.

## Articulation avec la facture papier et le PDF non structure

Pendant la phase transitoire, plusieurs supports coexistent. Une facture papier reste valide entre un assujetti francais qui n'est pas encore soumis a l'obligation d'emission (avant sa date d'application au 1er septembre 2027 pour les TPE) et un destinataire qui doit etre capable de la recevoir. Un PDF non structure, sans couche XML, n'est plus considere comme une facture electronique au sens de la reforme : il ne suffit pas a satisfaire l'obligation, meme s'il a ete signe electroniquement.

Pour eviter les ambiguites, l'administration recommande d'utiliser exclusivement le Factur-X (PDF + XML embarque) pour les emetteurs souhaitant conserver une representation visuelle. Cette approche presente l'avantage de la double lecture : le destinataire peut afficher le PDF s'il le souhaite, et son systeme d'information peut traiter directement le XML.

L'archivage probatoire impose une conservation de six ans a compter de la date de la derniere operation mentionnee. Les factures structurees doivent etre conservees dans un format conforme au reglement eIDAS et au Code des relations entre le public et l'administration. Une PDP propose en general un service d'archivage a valeur probante inclus ou en option.

## Ressources institutionnelles et mise a jour de la doctrine

La doctrine fiscale evolue a un rythme soutenu, en raison du caractere technique de la reforme et de la phase de montee en charge des plateformes. Plusieurs sources institutionnelles concentrent les informations a jour : le site impots.gouv.fr (DGFiP) regroupe la documentation officielle, le portail portailpro.gouv.fr decrit le fonctionnement du PPF, le BOFIP publie la doctrine administrative sous la reference BOI-TVA-DECLA-30, Legifrance heberge l'ordonnance n° 2021-1190, le decret n° 2022-1299 et la loi de finances 2024.

Pour une vision pedagogique du dispositif, consulter aussi la page dediee de **service-public.fr** et les fiches publiees par la **DGE** (Direction generale des entreprises) sur economie.gouv.fr. Les fiches Comparatif-Pro qui detaillent chaque facette du dispositif s'appuient sur ces sources, organisees autour de ce guide pilier et completees par des analyses sectorielles (PME, TPE, auto-entrepreneurs, choix de PDP, choix de format).

Pour sécuriser la transition, beaucoup d'entreprises s'appuient sur leur cabinet d'expertise comptable. Des réseaux comme In Extenso accompagnent les TPE et PME dans le choix de la plateforme, la mise en conformité des factures et l'adaptation des process comptables.

## FAQ

<details>
<summary>Qu'est-ce que la facturation electronique en 2026 ?</summary>

Il s'agit d'un dispositif obligatoire institue par l'ordonnance n° 2021-1190 du 15 septembre 2021 et le decret n° 2022-1299 du 7 octobre 2022. Toute facture entre assujettis a la TVA etablis en France doit etre transmise sous format structure (Factur-X, UBL ou CII conformes a la norme EN 16931) via le Portail Public de Facturation ou une plateforme de dematerialisation partenaire. Le dispositif s'accompagne d'une obligation de transmission de donnees (e-reporting) pour les operations B2C et internationales.
</details>

<details>
<summary>Quelles sont les dates cles du calendrier 2026-2027 ?</summary>

Le 1er septembre 2026, toutes les entreprises etablies en France doivent etre capables de recevoir des factures dematerialisees. A la meme date, les grandes entreprises et les ETI sont tenues d'emettre leurs factures au format structure et de transmettre leurs donnees de e-reporting. Le 1er septembre 2027, l'obligation d'emission est etendue aux PME et aux microentreprises (TPE, auto-entrepreneurs).
</details>

<details>
<summary>Qu'est-ce qu'une PDP et faut-il en choisir une ?</summary>

Une plateforme de dematerialisation partenaire est un operateur prive immatricule par la DGFiP. Elle assure la transmission des factures structurees et des donnees de e-reporting entre assujettis et vers l'administration fiscale. Le recours a une PDP n'est pas obligatoire, le Portail Public de Facturation reste accessible gratuitement, mais une PDP apporte des services additionnels (connecteurs ERP, archivage probatoire, gestion des cycles d'approbation, formats EDI proprietaires).
</details>

<details>
<summary>Quels formats sont autorises ?</summary>

Trois formats socles sont retenus : Factur-X (PDF/A-3 avec donnees XML embarquees), UBL 2.1 (Universal Business Language) et UN/CEFACT CII (Cross Industry Invoice). Tous trois respectent la norme europeenne EN 16931. Une PDP peut convertir un format proprietaire EDI vers l'un de ces trois socles avant transmission. Plus de details sur la [norme EN 16931](/blog/format-facture-electronique-factur-x-ubl-cii/).
</details>

<details>
<summary>Quelles sont les sanctions en cas de non-conformite ?</summary>

Le Code general des impots prevoit, a l'article 1737, une amende de 15 euros par facture non conforme dans la limite de 15 000 euros par annee civile pour le defaut d'emission au format electronique. L'absence de transmission des donnees de e-reporting est sanctionnee par une amende de 250 euros par transmission omise, plafonnee a 45 000 euros par an. Au-dela des sanctions financieres, l'entreprise s'expose a un risque de redressement TVA.
</details>
