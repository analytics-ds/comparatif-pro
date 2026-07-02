---
title: "PDP : plateforme de dematerialisation partenaire, role et choix | Comparatif-Pro"
translationKey: "pdp-facture-electronique"
date: "2026-05-07"
lastmod: "2026-05-07"
publishDate: "2026-05-07"
description: "PDP facture electronique : definition, role, immatriculation DGFiP, distinction PDP/PPF/OD/OC, criteres de choix et liste indicative des editeurs immatricules."
categories: ["Logiciels professionnels"]
tags: ["pdp", "facturation-electronique", "dgfip", "ppf", "iso-27001", "annuaire", "immatriculation"]
author: "thomas-durand"
image: "/images/blog/pdp-facture-electronique.jpg"
imageAlt: "Operatrice supervisant le routage d'une facture electronique via une plateforme de dematerialisation partenaire immatriculee"
imageCredit: "Image issue d'Openverse (CC BY)"
faq:
  - question: "Qu'est-ce qu'une PDP en facturation electronique ?"
    answer: "Une PDP (plateforme de dematerialisation partenaire) est un operateur prive immatricule par la DGFiP pour emettre, transmettre et recevoir les factures dematerialisees entre assujettis a la TVA etablis en France. Elle assure aussi la conversion entre formats (Factur-X, UBL, CII), l'archivage legal a valeur probante pendant dix ans, le e-reporting des donnees fiscales et la gestion des statuts de cycle de vie. Sans immatriculation effective, une plateforme ne peut pas exercer le role de PDP au sens de la reforme."
  - question: "Quelle est la difference entre PDP, PPF, OD et OC ?"
    answer: "Le PPF (Portail Public de Facturation), gere par l'AIFE, joue le role d'annuaire central et de concentrateur de donnees fiscales pour la DGFiP. La PDP est un operateur prive immatricule qui transmet les factures et qui peut les emettre, les recevoir, les convertir et les archiver. Un OD (operateur de dematerialisation) propose des services de dematerialisation mais n'est pas immatricule, il doit donc s'appuyer sur une PDP ou sur le PPF pour la transmission officielle. Un OC (operateur de communication) est un simple transporteur technique de flux entre deux plateformes, sans pouvoir agir en emetteur ou recepteur officiel."
  - question: "Comment verifier qu'une PDP est immatriculee ?"
    answer: "Le registre officiel des PDP immatriculees est tenu par la DGFiP et publie sur impots.gouv.fr. Il liste le numero d'immatriculation, le nom de l'editeur, la date de delivrance et la duree de validite (trois ans renouvelables). Une plateforme se declarant en cours d'immatriculation n'apparait pas dans le registre tant que la procedure n'est pas finalisee. Une bonne pratique consiste a exiger contractuellement la communication du numero d'immatriculation effectif avant toute mise en production."
  - question: "Combien coute une PDP pour une PME ?"
    answer: "Les tarifs varient fortement selon le volume de factures, le perimetre fonctionnel et les integrations comptables. Les offres d'entree de gamme demarrent autour de 9 a 15 euros HT par mois pour une TPE qui emet quelques dizaines de factures, et peuvent depasser plusieurs milliers d'euros mensuels pour un groupe ETI multi-filiales avec connecteurs ERP, archivage avance et flux EDI. Les criteres qui font varier la facture sont le volume mensuel, le nombre d'utilisateurs, le nombre de societes geres et le niveau de support."
  - question: "Une entreprise peut-elle utiliser plusieurs PDP en meme temps ?"
    answer: "Oui, rien dans le decret 2022-1299 n'empeche une entreprise de declarer plusieurs PDP dans l'annuaire central : une pour l'emission, une autre pour la reception, voire des PDP differentes par filiale ou par flux. L'annuaire de la DGFiP gere ces configurations multiples et indique a l'emetteur quelle plateforme cibler pour chaque destinataire. Cette flexibilite reste rare en pratique car elle complique l'archivage et le pilotage. La majorite des entreprises retiennent une PDP unique."
readingTime: true
---

La **pdp facture electronique** designe l'operateur prive immatricule par la DGFiP qui transmet les factures dematerialisees entre assujettis a la TVA etablis en France. Avec le Portail Public de Facturation (PPF), la PDP forme l'epine dorsale technique de la reforme issue de l'ordonnance n° 2021-1190 et du decret n° 2022-1299. A partir du 1er septembre 2026, toute facture B2B domestique doit transiter par l'une de ces plateformes pour etre opposable et integree au pre-remplissage des declarations de TVA.

L'immatriculation, prevue par l'arrete du 22 juin 2023 portant cahier des charges des PDP, n'a rien d'une simple formalite declarative. Elle suppose un audit de securite ISO 27001, une validation par l'ANSSI, un dossier technique conforme aux specifications de la DGFiP et la signature d'une convention triennale renouvelable. Cette barriere a l'entree distingue la PDP des autres acteurs du marche, notamment des operateurs de dematerialisation (OD) et des operateurs de communication (OC) qui ne disposent pas du meme statut.

> **En bref :**
> 1. La PDP est un operateur prive immatricule par la DGFiP, habilite a emettre, transmettre, recevoir, convertir et archiver les factures dematerialisees inter-entreprises.
> 2. L'immatriculation suppose un audit ISO 27001, une validation ANSSI et la conformite a l'arrete du 22 juin 2023, pour une duree initiale de trois ans renouvelable.
> 3. La PDP differe du PPF (annuaire public, concentrateur fiscal), de l'OD (non immatricule) et de l'OC (simple transporteur technique).
> 4. Le registre officiel des PDP est publie par la DGFiP sur impots.gouv.fr et constitue la seule source faisant foi pour verifier l'immatriculation effective d'un editeur.

## Definition d'une plateforme de dematerialisation partenaire

Une plateforme de dematerialisation partenaire est un operateur prive, immatricule par la Direction generale des Finances publiques, qui rend des services de transmission, de conversion et d'archivage des factures pour le compte d'une ou plusieurs entreprises assujetties a la TVA. Le statut juridique de la PDP est defini par l'article 290 B du Code general des impots, introduit par l'ordonnance du 15 septembre 2021 et precise par le decret du 7 octobre 2022.

Trois caracteristiques distinguent une PDP d'un simple editeur de logiciel de facturation :

- L'immatriculation par la DGFiP, materialisee par un numero unique inscrit au registre officiel.
- La capacite a transmettre des donnees fiscales directement vers le concentrateur public, sans passer par le PPF en cas de flux entre deux PDP.
- L'engagement contractuel sur des obligations specifiques : conservation des donnees, niveau de service, signalement des incidents, audits de conformite.

La PDP n'a pas vocation a remplacer l'editeur de gestion ou l'ERP de l'entreprise. Elle vient s'interfacer en aval, soit directement embarquee dans un logiciel de comptabilite, soit en mode service connecte par API. Pour saisir le contexte plus large dans lequel elle s'inscrit, le [guide complet de la facturation electronique](/blog/guide-facturation-electronique/) detaille l'ensemble des dispositifs reglementaires et techniques.

> "Les plateformes de dematerialisation partenaires constituent l'un des piliers de l'architecture cible. Leur immatriculation garantit aux entreprises et a l'administration un haut niveau de fiabilite, d'interoperabilite et de securite des echanges."
> -- Direction generale des Finances publiques, impots.gouv.fr, 2024

## PDP vs PPF vs OD vs OC : quatre acteurs distincts

L'ecosysteme de la dematerialisation des factures repose sur une chaine d'acteurs aux roles complementaires. Confondre PDP, PPF, OD et OC est une erreur frequente qui peut conduire a un mauvais choix de prestataire ou a un defaut de conformite. Le tableau ci-dessous synthetise les differences fondamentales.

| Acteur | Statut | Role principal | Immatricule DGFiP | Peut emettre une facture officielle |
|---|---|---|---|---|
| PPF (Portail Public de Facturation) | Operateur public, gere par l'AIFE | Annuaire central, concentrateur fiscal, plateforme gratuite de secours | Sans objet (operateur public) | Oui |
| PDP (plateforme de dematerialisation partenaire) | Operateur prive immatricule | Emission, transmission, reception, conversion de format, archivage legal, e-reporting | Oui (numero officiel, registre public) | Oui |
| OD (operateur de dematerialisation) | Operateur prive non immatricule | Services de dematerialisation amont ou aval (saisie, conversion, integration ERP) | Non | Non, doit passer par une PDP ou le PPF |
| OC (operateur de communication) | Operateur prive non immatricule | Transport technique des flux entre deux plateformes (EDI, API, AS4) | Non | Non, jamais en position d'emetteur ou recepteur officiel |

Le PPF, adosse a l'infrastructure Chorus Pro et gere par l'Agence pour l'Informatique Financiere de l'Etat, joue trois roles : annuaire central qui repertorie chaque entreprise et indique sa plateforme de reception, concentrateur de donnees fiscales destine a la DGFiP, et plateforme gratuite de secours pour les structures qui n'auraient pas choisi de PDP. La PDP, elle, est un operateur prive a service etendu : interfaces utilisateur, connecteurs comptables, archivage probatoire, suivi des statuts de cycle de vie, reporting metier.

L'OD se positionne en amont ou en aval de la PDP. Un cabinet d'expertise comptable qui scanne et integre des factures fournisseurs sans transmettre directement au PPF est typiquement un OD. L'OC est encore plus en retrait : il assure le transport technique des flux entre deux plateformes, par exemple via les protocoles EDI, AS4 ou des API specifiques, sans agir comme emetteur ou recepteur officiel. Le [role de la DGFiP dans la facturation electronique](/blog/facturation-electronique-dgfip/) precise le partage des responsabilites entre administration et operateurs prives.

## Le processus d'immatriculation d'une PDP

L'immatriculation d'une plateforme par la DGFiP est un parcours encadre par l'arrete du 22 juin 2023 portant cahier des charges des plateformes de dematerialisation partenaires. La procedure s'etale generalement sur six a douze mois pour un editeur deja outille, et peut depasser dix-huit mois pour une structure qui doit construire son socle de conformite a partir de zero.

Le dossier d'immatriculation comporte plusieurs blocs :

- Une preuve d'immatriculation au registre du commerce et des societes en France ou dans un Etat membre de l'Union europeenne.
- La description detaillee de l'architecture technique, des formats geres, des protocoles supportes (API REST, EDI, AS4) et des modalites d'archivage.
- Un rapport d'audit de securite delivre par un auditeur PASSI ou par un organisme accredite, attestant de la conformite ISO 27001 du systeme d'information et de l'application des regles de l'ANSSI.
- Une convention signee avec la DGFiP, d'une duree de trois ans renouvelable, listant les engagements de l'operateur en matiere de qualite de service, de signalement d'incident et d'auditabilite.
- Le respect des regles de proprete, de non-repudiation et de tracabilite des flux, en coherence avec le [calendrier de la facturation electronique](/blog/calendrier-facturation-electronique/).

L'audit ISO 27001 porte sur l'ensemble du systeme de management de la securite de l'information : cartographie des risques, gestion des acces, journalisation, plan de continuite, sauvegardes, gestion des prestataires sous-traitants. La validation ANSSI s'attache plus particulierement aux mecanismes cryptographiques (signature electronique, scellement, chiffrement des transmissions), a la qualification des modules cryptographiques et au respect des recommandations du Referentiel general de securite.

Une fois le dossier accepte, la DGFiP delivre un numero d'immatriculation et publie l'editeur dans le registre officiel sur impots.gouv.fr. La duree initiale est de trois ans, avec un audit intermediaire prevu a mi-parcours. Toute defaillance grave (perte d'immatriculation, manquement aux obligations de transmission) entraine la radiation du registre et oblige les clients de la PDP concernee a basculer en urgence vers un autre operateur ou vers le PPF.

## Les fonctions operationnelles d'une PDP

Une PDP n'est pas un simple tuyau. Le cahier des charges DGFiP impose un socle fonctionnel etoffe, qui couvre l'ensemble du cycle de vie d'une facture, de son emission a son archivage en passant par la collecte des donnees fiscales.

Les fonctions structurantes sont au nombre de huit :

- Emission d'une facture conforme a la norme europeenne EN 16931, dans l'un des formats normalises (Factur-X, UBL 2.1, CII).
- Transmission au destinataire via le canal indique par l'annuaire central du PPF, qu'il s'agisse d'une autre PDP ou du PPF lui-meme.
- Reception d'une facture entrante avec controle de conformite, verification de signature et notification au destinataire.
- Conversion de format si l'emetteur et le destinataire utilisent des formats differents, dans le respect du jeu de donnees minimal defini par la DGFiP.
- Archivage legal a valeur probante pendant dix ans, conformement a l'article L102 B du Livre des procedures fiscales.
- E-reporting des donnees de paiement et des operations non couvertes par la facturation electronique (B2C, international, acquisitions intracommunautaires).
- Gestion des statuts de cycle de vie (depose, recu, accepte, refuse, mis en paiement, paye), transmis a l'administration et au partenaire.
- Mise a jour de l'annuaire en lecture continue, pour identifier la plateforme de reception du destinataire au moment de l'emission.

Le statut de cycle de vie est l'un des elements les plus structurants de la reforme. Chaque transition est horodatee, signee et transmise au PPF, qui retransmet l'information aux deux parties et a la DGFiP. Le suivi des statuts permet de tracer une facture de bout en bout et alimente le contentieux en cas de litige sur une echeance ou un paiement.

## Parcours type d'une facture via une PDP

Le scenario standard d'emission d'une facture via une PDP suit un enchainement reglemente par le decret 2022-1299 et detaille dans les specifications externes publiees sur impots.gouv.fr.

- Etape 1 : l'editeur de gestion de l'emetteur produit la facture au format pivot (en general Factur-X) et la transmet a sa PDP via une API ou un connecteur.
- Etape 2 : la PDP controle la conformite des donnees obligatoires (numero SIREN, mentions legales, montants, codification TVA) et signe electroniquement la facture.
- Etape 3 : la PDP interroge l'annuaire central du PPF pour identifier la plateforme de reception du destinataire (autre PDP ou PPF).
- Etape 4 : la PDP transmet la facture a la plateforme cible via un canal interoperable (API REST, AS4, EDI selon les conventions techniques).
- Etape 5 : la plateforme du destinataire recoit la facture, la met a disposition dans son interface client et notifie l'utilisateur.
- Etape 6 : le destinataire emet un statut de cycle de vie (recu, accepte, refuse partiellement ou totalement), retransmis a l'emetteur et a la DGFiP.
- Etape 7 : les donnees fiscales (jeu de donnees minimal) sont extraites et envoyees au concentrateur public, qui alimente le pre-remplissage de la TVA.
- Etape 8 : la PDP archive la facture pour une duree minimale de dix ans, avec scellement horodate et journal d'audit.

Tout le parcours est instrumente. Une transmission qui echoue declenche un statut d'erreur tracable. Un format non conforme est rejete avec un code d'erreur normalise. Cette mecanique vise a securiser les flux et a fiabiliser le pre-remplissage des declarations de TVA, conformement a l'objectif de lutte anti-fraude inscrit dans la [reforme des plateformes de facturation electronique](/blog/comparatif-plateformes-facturation-electronique/).

## Editeurs immatricules et candidats : panorama indicatif

Le registre officiel des PDP est evolutif. Les premiers numeros d'immatriculation ont ete attribues a partir de 2024, et la liste s'enrichit au fil des audits. Le tableau ci-dessous donne un panorama indicatif des editeurs immatricules ou en cours d'immatriculation, a verifier systematiquement sur impots.gouv.fr avant tout engagement contractuel.

| Editeur | Statut indicatif | Cible principale | Particularite |
|---|---|---|---|
| Pennylane | Immatricule | TPE, PME | Approche unifiee comptabilite et facturation, reseau d'experts-comptables partenaires |
| Sage | Immatricule | PME, ETI, grands comptes | Connecteur natif aux suites Sage 100, Sage X3, Sage FRP 1000 |
| Cegid | Immatricule | PME, ETI, secteur public | Integration aux solutions Cegid XRP, Cegid Quadra, Yourcegid |
| Yooz | Immatricule | TPE, PME | Specialiste de la dematerialisation des factures fournisseurs, capture intelligente |
| Esker | Immatricule | ETI, grands comptes | Plateforme cloud de gestion des cycles order-to-cash et procure-to-pay |
| Generix | Immatricule | ETI, retail, supply chain | Heritage EDI fort, interoperabilite avec les flux logistiques |
| Docaposte | Immatricule | Grands comptes, secteur public | Filiale numerique du groupe La Poste, valeur probante reconnue |
| Iopole | En cours d'immatriculation | TPE, PME, experts-comptables | Plateforme operee depuis la France, positionnement souverain |
| Tiime | En cours d'immatriculation | TPE, PME, micro-entrepreneurs | Couplage facturation, comptabilite et services bancaires |
| EBP | En cours d'immatriculation | TPE, PME | Editeur historique du marche francais, large parc installe |
| Indy | En cours d'immatriculation | Independants, professions liberales | Application mobile orientee comptabilite simplifiee |
| Axonaut | En cours d'immatriculation | TPE, petites PME | Suite tout-en-un (CRM, devis, facturation, comptabilite legere) |

Le statut d'immatriculation peut evoluer rapidement. Une plateforme reprise dans cette liste n'est pas necessairement immatriculee a la date de lecture, et l'inverse est egalement possible. Pour un panorama plus large des solutions disponibles, le [comparatif des logiciels de facturation electronique](/blog/meilleur-logiciel-facturation-electronique/) detaille les fonctions, les tarifs et les positionnements, en complement de la verification d'immatriculation faite sur impots.gouv.fr.

## Criteres de choix d'une PDP

Le choix d'une PDP ne se resume pas a l'immatriculation. Les ecarts fonctionnels et tarifaires entre operateurs sont importants, et la decision engage l'entreprise sur plusieurs annees compte tenu des couts de migration, de la duree d'archivage et des integrations comptables.

Sept criteres meritent une analyse fine :

- Immatriculation effective, et non simple statut declaratif. Verifier le numero sur le registre DGFiP, demander la copie de la convention triennale et la date du dernier audit ISO 27001.
- Formats supportes en emission et en reception : Factur-X, UBL 2.1, CII, et selon les besoins ZUGFeRD ou autres profils sectoriels. Une PDP qui refuse un format peut imposer une conversion qui degrade les donnees.
- Connecteurs comptables et ERP : pre-integration native a Sage, Cegid, EBP, Pennylane, SAP, Microsoft Dynamics, Oracle, Odoo. La qualite du connecteur conditionne la fluidite operationnelle et le cout d'integration.
- Tarification : grille par volume mensuel, par utilisateur, par societe. Couts d'archivage, couts de conversion de format, couts de support premium, frais d'onboarding initial.
- Niveau de support : SLA contractuels, langues couvertes, plages horaires, gestion des incidents critiques, accompagnement a la mise en service.
- Certifications complementaires : NF525 pour les caisses, qualification eIDAS pour les services de signature, certification SOC 2 pour les controles internes, agrement HDS si l'archivage couvre des donnees de sante.
- Trajectoire produit : feuille de route documentee, equipes dediees a la conformite reglementaire, capacite a suivre les evolutions DGFiP (e-reporting etendu, nouveaux statuts, format CTC europeen ViDA).

Le contexte sectoriel pese aussi. Une ETI industrielle privilegiera une PDP avec ancrage EDI fort et connecteur ERP robuste. Une TPE de services s'orientera vers une plateforme proche d'un logiciel de comptabilite cloud, avec un onboarding rapide. Un cabinet d'expertise comptable cherchera une PDP multi-clients qui s'integre dans son outillage de production et qui supporte la facturation pour le compte de tiers.

## Verification de l'immatriculation : registre DGFiP et API d'annuaire

La verification systematique du statut d'immatriculation est un reflexe de conformite. Deux outils officiels permettent de s'assurer qu'un editeur dispose bien des droits requis pour exercer le role de PDP.

Le registre des PDP immatriculees est publie sur impots.gouv.fr, dans la rubrique consacree a la facturation electronique. Il liste pour chaque operateur le nom commercial, le numero SIREN, le numero d'immatriculation, la date de delivrance, la duree de validite et le perimetre fonctionnel couvert. La consultation est libre. Le registre fait foi en cas de litige : un editeur non present ne peut pas se prevaloir du statut, meme s'il declare une procedure en cours.

L'API d'annuaire, publiee par le PPF et documentee par l'AIFE, permet aux PDP, aux ERP et aux logiciels de gestion d'interroger en continu la liste des destinataires et leur plateforme de reception. C'est cette API qui rend possible le routage automatique d'une facture vers le bon canal. Elle est mise a jour en quasi temps reel, ce qui evite a l'emetteur de gerer manuellement un annuaire fournisseurs. La couverture fonctionnelle minimale d'une PDP inclut l'interrogation reguliere de cette API et la mise a jour des partenaires emission et reception dans son referentiel interne.

Trois bonnes pratiques completent ce dispositif :

- Inscrire dans le contrat de service avec la PDP une clause de rappel d'immatriculation, qui oblige l'editeur a notifier sans delai toute perte ou suspension de son statut.
- Auditer une fois par an la presence de la PDP au registre, idealement en lien avec la cloture comptable ou la revision du plan de continuite.
- Verifier que la PDP publie ses preuves d'audit ISO 27001 et son rapport SOC 2 ou equivalent sur demande, en complement du numero d'immatriculation.

Pour anticiper les choix de format et la negociation des conventions, l'article dedie aux [formats UBL et CII](/blog/format-facture-electronique-factur-x-ubl-cii/) detaille les specificites techniques que chaque PDP doit savoir traiter, et explicite les implications du jeu de donnees minimal exige par la DGFiP.

## Risques associes a un mauvais choix de PDP

Un choix mal calibre expose l'entreprise a plusieurs risques, certains immediats, d'autres latents.

- Risque de conformite : recours a un editeur non immatricule presente comme PDP. Les factures emises ou recues via cet operateur ne sont pas opposables au sens de la reforme et peuvent etre rejetees au pre-remplissage de la TVA, declenchant des relances administratives.
- Risque de dependance technique : verrouillage par des formats proprietaires ou par des contrats de longue duree sans clause de reversibilite. Une migration depuis une PDP vers une autre suppose la portabilite des archives et l'accessibilite des journaux de cycle de vie sur dix ans.
- Risque operationnel : indisponibilite recurrente, retards dans les transmissions, incidents non resolus dans les delais contractuels. Un SLA flou ou non documente est un signal d'alerte.
- Risque tarifaire : grilles complexes avec couts caches sur les volumes pic, sur la conversion de format ou sur les integrations supplementaires. La comparaison budgetaire suppose une simulation sur la base d'un volume reel, pas d'une moyenne theorique.
- Risque juridique : non-conformite aux obligations d'archivage probatoire, defaut de signalement d'incident, defaillance de la convention DGFiP. La perte d'immatriculation declenchee par un audit non passe oblige a basculer en urgence et peut entrainer des couts de transition significatifs.

La parade tient en quelques points fermes : verification du registre, analyse contractuelle ligne a ligne, simulation de migration, plan de continuite documente, suivi des indicateurs de qualite de service trimestre par trimestre. La consultation du dossier juridique disponible sur Legifrance, en particulier l'arrete du 22 juin 2023 et l'article 41 du decret 2022-1299, permet de cadrer les exigences minimales attendues d'un prestataire serieux.

## Synthese : la PDP au coeur de la mecanique fiscale

La PDP est plus qu'un sous-traitant technique. Elle agit comme un tiers de confiance entre les entreprises et la DGFiP, garantit l'integrite et la tracabilite des flux, et porte des engagements reglementaires propres. Sa selection merite une grille d'analyse stricte, fondee sur l'immatriculation effective, la robustesse du socle fonctionnel et la solidite contractuelle.

Trois reperes pour structurer la decision :

- Verifier l'immatriculation au registre officiel publie sur impots.gouv.fr, sans se contenter d'une declaration commerciale.
- Aligner le choix avec les contraintes metier : volumes, integrations comptables, sectoriel, archivage, multi-pays.
- Documenter les engagements contractuels (SLA, audits, reversibilite) et prevoir un plan de continuite en cas de defaillance de la PDP retenue.

Pour completer la perspective et croiser le sujet PDP avec la mecanique generale de la reforme, le [calendrier de la facturation electronique](/blog/calendrier-facturation-electronique/) precise les jalons d'application de chaque obligation.

Le choix d'une PDP engage l'entreprise sur plusieurs années. Votre expert-comptable peut objectiver ce choix, des cabinets comme In Extenso comparent les plateformes au regard des flux réels de l'entreprise.

## FAQ

<details>
<summary>Qu'est-ce qu'une PDP en facturation electronique ?</summary>

Une PDP (plateforme de dematerialisation partenaire) est un operateur prive immatricule par la DGFiP pour emettre, transmettre et recevoir les factures dematerialisees entre assujettis a la TVA etablis en France. Elle assure aussi la conversion entre formats (Factur-X, UBL, CII), l'archivage legal a valeur probante pendant dix ans, le e-reporting des donnees fiscales et la gestion des statuts de cycle de vie. Sans immatriculation effective, une plateforme ne peut pas exercer le role de PDP au sens de la reforme.
</details>

<details>
<summary>Quelle est la difference entre PDP, PPF, OD et OC ?</summary>

Le PPF (Portail Public de Facturation), gere par l'AIFE, joue le role d'annuaire central et de concentrateur de donnees fiscales pour la DGFiP. La PDP est un operateur prive immatricule qui transmet les factures et qui peut les emettre, les recevoir, les convertir et les archiver. Un OD (operateur de dematerialisation) propose des services de dematerialisation mais n'est pas immatricule, il doit donc s'appuyer sur une PDP ou sur le PPF pour la transmission officielle. Un OC (operateur de communication) est un simple transporteur technique de flux entre deux plateformes, sans pouvoir agir en emetteur ou recepteur officiel.
</details>

<details>
<summary>Comment verifier qu'une PDP est immatriculee ?</summary>

Le registre officiel des PDP immatriculees est tenu par la DGFiP et publie sur impots.gouv.fr. Il liste le numero d'immatriculation, le nom de l'editeur, la date de delivrance et la duree de validite (trois ans renouvelables). Une plateforme se declarant en cours d'immatriculation n'apparait pas dans le registre tant que la procedure n'est pas finalisee. Une bonne pratique consiste a exiger contractuellement la communication du numero d'immatriculation effectif avant toute mise en production.
</details>

<details>
<summary>Combien coute une PDP pour une PME ?</summary>

Les tarifs varient fortement selon le volume de factures, le perimetre fonctionnel et les integrations comptables. Les offres d'entree de gamme demarrent autour de 9 a 15 euros HT par mois pour une TPE qui emet quelques dizaines de factures, et peuvent depasser plusieurs milliers d'euros mensuels pour un groupe ETI multi-filiales avec connecteurs ERP, archivage avance et flux EDI. Les criteres qui font varier la facture sont le volume mensuel, le nombre d'utilisateurs, le nombre de societes geres et le niveau de support.
</details>

<details>
<summary>Une entreprise peut-elle utiliser plusieurs PDP en meme temps ?</summary>

Oui, rien dans le decret 2022-1299 n'empeche une entreprise de declarer plusieurs PDP dans l'annuaire central : une pour l'emission, une autre pour la reception, voire des PDP differentes par filiale ou par flux. L'annuaire de la DGFiP gere ces configurations multiples et indique a l'emetteur quelle plateforme cibler pour chaque destinataire. Cette flexibilite reste rare en pratique car elle complique l'archivage et le pilotage. La majorite des entreprises retiennent une PDP unique.
</details>
