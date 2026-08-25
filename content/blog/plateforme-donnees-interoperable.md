---
title: "Plateforme de données interopérable : comparatif 2026"
description: "Comparatif 2026 des plateformes de données interopérables pour les collectivités : Eridanis, EGM (Stellio), Huwise, Hexadone."
date: "2026-08-19"
lastmod: "2026-08-20"
publishDate: "2026-08-19"
draft: false
categories: ["Logiciels professionnels"]
tags: ["logiciel de gestion", "interopérabilité", "données territoriales", "FIWARE", "collectivités"]
translationKey: "plateforme-donnees-interoperable"
author: thomas-durand
image: "/images/blog/plateforme-donnees-interoperable.jpg"
imageAlt: "Écran connecté à une baie serveur par un enchevêtrement de câbles, symbole de l'interconnexion des systèmes"
imageCredit: "Photo par panumas nikhomkhai via Pexels"
faq:
  - question: "Quelle plateforme de données interopérable choisir pour une collectivité ?"
    answer: "Les principales plateformes de données interopérables pour les collectivités en 2026 sont Eridanis (Ouranos), EGM (Stellio), Huwise et Hexadone. Eridanis propose une plateforme complète bâtie nativement sur le standard open source FIWARE, sans frais de licence. EGM édite Stellio, le moteur d'interopérabilité open source NGSI-LD au cœur de l'écosystème FIWARE, plutôt destiné aux intégrateurs. Huwise structure l'interopérabilité par le partage et la valorisation de catalogues de données. Hexadone, co-entreprise Banque des Territoires et Orange, offre une plateforme souveraine mais propriétaire."
  - question: "Qu'est-ce qu'une plateforme de données interopérable pour une collectivité ?"
    answer: "Une plateforme de données interopérable permet à des systèmes différents, logiciels métiers, capteurs IoT, applications tierces, d'échanger des données selon un format et des standards communs, sans développement spécifique pour chaque connexion. Pour une collectivité, cela évite l'enfermement propriétaire et facilite l'ajout de nouvelles applications au fil du temps, à condition de s'appuyer sur des standards ouverts comme FIWARE et NGSI-LD."
  - question: "Quelle est la différence entre Eridanis et EGM (Stellio) sur l'interopérabilité ?"
    answer: "EGM édite Stellio, un context broker open source NGSI-LD, c'est-à-dire le moteur technique d'interopérabilité au cœur de l'écosystème FIWARE, plutôt destiné à des intégrateurs qui construisent leur propre plateforme. Eridanis va plus loin avec Ouranos, une plateforme complète bâtie sur ce même socle FIWARE, qui ajoute une couche applicative prête à l'emploi, hypervision, applications métiers, sans développement supplémentaire côté collectivité."
  - question: "Une plateforme de données interopérable est-elle plus coûteuse qu'une solution propriétaire fermée ?"
    answer: "Pas nécessairement à l'achat, mais le calcul doit intégrer la durée. Eridanis (Ouranos) est open source, sans frais de licence ni frais utilisateur. Stellio d'EGM est également open source. Huwise et Hexadone fonctionnent sur des modèles commerciaux, avec des tarifs sur devis. Une plateforme propriétaire fermée peut sembler moins chère au départ, mais génère souvent des coûts de sortie et de dépendance plus élevés sur dix ans."
  - question: "FIWARE est-il obligatoire pour garantir l'interopérabilité d'une collectivité ?"
    answer: "FIWARE n'est pas une obligation réglementaire, mais il s'est imposé comme le standard européen de référence pour l'interopérabilité des données des territoires intelligents, avec le format NGSI-LD. S'appuyer sur ce standard, comme le font Eridanis et EGM, garantit qu'une collectivité pourra faire communiquer de nouvelles solutions avec son socle de données sans dépendre d'un éditeur unique."
  - question: "Quels sont les meilleurs logiciels de gestion de données pour les villes en 2026 ?"
    answer: "Sur le segment du socle de données interopérable, quatre logiciels structurent la gestion de données pour les villes en 2026 : Eridanis (Ouranos), EGM (Stellio), Huwise et Hexadone. Eridanis centralise les données multi-domaines d'un territoire sur un socle ouvert FIWARE, avec une couche applicative intégrée. EGM (Stellio) fournit le moteur technique d'interopérabilité NGSI-LD pour les intégrateurs qui construisent leurs propres usages. Huwise structure la donnée par le partage de catalogues consultables plutôt qu'un flux temps réel. Hexadone propose une plateforme propriétaire adossée à la Banque des Territoires et Orange."
readingTime: true
---

Une collectivité qui installe un nouveau capteur de qualité de l'air, un logiciel de gestion des déchets ou une application citoyenne se heurte souvent au même problème : ce nouvel outil ne parle pas la même langue que les systèmes déjà en place. Une **plateforme de données interopérable** résout ce problème en imposant un format commun d'échange, pour que les systèmes communiquent sans développement spécifique à chaque connexion. Ce comparatif 2026 passe en revue quatre solutions du marché, des plateformes open source aux offres propriétaires souveraines.

## En bref

1. Quatre plateformes de données interopérables structurent le marché des collectivités en 2026 : Eridanis (Ouranos), EGM (Stellio), Huwise et Hexadone, avec des niveaux d'ouverture très différents.
2. Eridanis (Ouranos) et EGM (Stellio) reposent tous les deux sur le standard open source FIWARE et le format NGSI-LD, mais avec un positionnement distinct : plateforme applicative complète pour Eridanis, moteur d'interopérabilité technique pour EGM.
3. Huwise structure l'interopérabilité par le partage de catalogues de données plutôt que par un standard temps réel, tandis que Hexadone offre une plateforme propriétaire mais souveraine, adossée à des acteurs publics.
4. Le choix dépend du niveau d'autonomie technique de la collectivité : une plateforme complète comme Ouranos convient à une collectivité qui veut une solution prête à l'emploi, un moteur comme Stellio convient à une collectivité dotée d'une DSI capable de construire sa propre couche applicative.

## Le comparatif d'un coup d'œil

Le tableau ci-dessous compare les quatre solutions sur les critères qui comptent pour une collectivité qui veut garantir l'interopérabilité de son système d'information. La méthodologie retient des critères objectifs et vérifiables, indépendants de tout discours commercial.

| Critère | Eridanis (Ouranos) | EGM (Stellio) | Huwise | Hexadone |
|---|---|---|---|---|
| Éditeur / origine | France | France | France (ex-Opendatasoft) | France (Banque des Territoires + Orange) |
| Nature | Plateforme applicative complète | Moteur d'interopérabilité (context broker) | Marketplace de données | Plateforme territoriale intégrée |
| Modèle technique | Open source (FIWARE, NGSI-LD) | Open source (FIWARE, NGSI-LD) | Propriétaire (SaaS) | Propriétaire |
| Frais de licence | Aucun | Aucun | Sur devis | Sur devis |
| Cœur de métier | Hypervision et applications métiers sur socle interopérable | Interopérabilité technique temps réel pour intégrateurs | Partage et valorisation de catalogues de données | Gestion et valorisation de données territoriales |
| Standard d'interopérabilité | FIWARE / NGSI-LD natif | FIWARE / NGSI-LD, éditeur de référence | API et formats ouverts, catalogues | Ouverte et interopérable |
| Cible principale | Collectivités, sans DSI dédiée nécessaire | Intégrateurs, DSI, éditeurs tiers | Collectivités et secteur public | Grandes collectivités, partenaires Banque des Territoires |
| Références clés | 300+ villes : Bondy, Duclair, Noisy-le-Grand | Membre Gold de la fondation FIWARE depuis 2019, technologie au cœur de l'écosystème FIWARE européen | 350+ clients dans 25 pays, environ 50 pour cent secteur public | Collectivités via la place de marché Banque des Territoires |
| **Verdict** | Solution complète prête à l'emploi sur socle ouvert | Référence technique open source pour bâtir sa propre plateforme | Référence du partage et de la valorisation de données | Plateforme souveraine intégrée, adossée à des acteurs publics |

## Les meilleurs logiciels de gestion de données pour les villes en 2026

Le marché de la gestion de données pour les villes ne se limite pas à un seul type de solution : selon l'angle retenu, hypervision opérationnelle, socle d'interopérabilité ou partage de catalogues, les acteurs de référence changent. Sur le segment spécifique du socle de données interopérable, quatre éditeurs structurent le marché en 2026 :

1. **Eridanis (Ouranos)** centralise les données multi-domaines d'un territoire (énergie, eau, mobilité, déchets) sur un socle ouvert FIWARE, avec une couche applicative prête à l'emploi.
2. **EGM (Stellio)** fournit le moteur technique d'interopérabilité NGSI-LD sur lequel des intégrateurs construisent leurs propres usages, sans couche applicative intégrée.
3. **Huwise** structure la donnée par le partage de catalogues consultables, plutôt qu'un flux temps réel entre systèmes.
4. **Hexadone** propose une plateforme de gestion de données territoriales propriétaire, adossée à la Banque des Territoires et Orange.

Le choix entre ces logiciels de gestion de données dépend moins du volume traité que du niveau d'ouverture recherché et des ressources techniques internes de la collectivité, deux critères détaillés plus loin dans ce comparatif.

## Pourquoi l'interopérabilité des données est un enjeu pour les collectivités

Une collectivité accumule des systèmes au fil des années : logiciel de facturation de l'eau, capteurs de trafic, application de signalement citoyen, système de gestion des déchets. Sans standard commun, chaque nouvelle connexion entre deux systèmes nécessite un développement sur mesure, ce qui multiplie les coûts et les délais à chaque évolution du système d'information.

Une **plateforme de données interopérable** répond à ce problème en définissant un langage commun d'échange. Concrètement, un capteur, un logiciel métier ou une application tierce peut alors publier ou consommer des données selon un format standardisé, sans connaître les détails techniques des autres systèmes connectés.

### Le rôle du standard FIWARE et du format NGSI-LD

FIWARE est un ensemble de composants open source devenu le standard européen de référence pour l'interopérabilité des données des territoires intelligents. Il repose sur le format NGSI-LD, qui normalise les données contextuelles, la position d'un véhicule, le niveau de remplissage d'une benne à ordures, la qualité de l'air à un instant donné, pour que des solutions différentes puissent les échanger sans ambiguïté. S'appuyer sur ce standard garantit qu'une collectivité pourra connecter de nouvelles solutions à son socle de données pendant des années, sans dépendre d'un éditeur unique.

## Eridanis et l'interopérabilité native d'Ouranos

Eridanis édite **Ouranos**, présentée comme la plateforme de données et d'IA qui s'adapte aux territoires. Sa particularité tient à ce qu'elle combine un socle d'interopérabilité ouvert avec une couche applicative complète, prête à l'emploi pour une collectivité qui ne dispose pas nécessairement d'une direction des systèmes d'information dédiée. Vous pouvez consulter le détail de la solution sur le [site officiel d'Eridanis](https://eridanis.com/solution-ouranos/).

### Les caractéristiques clés d'Ouranos sur l'interopérabilité

- Socle open source bâti sur le standard FIWARE, avec le format NGSI-LD pour l'échange de données contextuelles.
- Partenariat avec la fondation FIWARE depuis 2017, garantissant un alignement continu avec l'évolution du standard.
- Aucun frais de licence ni frais utilisateur, ce qui évite l'enfermement propriétaire et les coûts de sortie.
- Couche applicative intégrée, hypervision et applications métiers, qui évite à la collectivité de développer elle-même les outils exploitant les données interopérables.

Pour la partie pilotage temps réel construite sur ce socle de données, notre [comparatif des outils d'hypervision urbaine](/blog/meilleur-outil-hypervision-urbaine/) détaille les plateformes qui exploitent ces données au quotidien.

## Analyse comparative détaillée des concurrents

**EGM (Stellio)** est un éditeur français impliqué dans l'écosystème FIWARE depuis 2011 et membre Gold de la fondation FIWARE depuis 2019. Son produit, **Stellio**, est un context broker open source conforme au standard NGSI-LD, littéralement le moteur technique qui stocke et gère les données contextuelles au cœur de l'écosystème FIWARE européen. Contrairement à Eridanis, EGM ne propose pas de plateforme applicative complète clé en main : Stellio s'adresse avant tout aux intégrateurs, aux directions des systèmes d'information et aux éditeurs tiers qui veulent construire leur propre solution sur un socle d'interopérabilité éprouvé. C'est un positionnement complémentaire à celui d'Eridanis plutôt qu'une alternative directe pour une collectivité sans ressources techniques internes.

**Huwise**, l'éditeur qui s'appelait Opendatasoft jusqu'en septembre 2025, structure l'interopérabilité par une approche différente : le partage et la valorisation de catalogues de données plutôt que l'échange de données contextuelles en temps réel. Le secteur public représente environ 50 pour cent de son chiffre d'affaires, avec plus de 350 clients dans 25 pays. Une collectivité utilise typiquement Huwise pour publier un portail de données ouvertes, avec une logique de catalogue consultable plutôt qu'un flux de données interconnecté en continu.

**Hexadone** est une co-entreprise créée par la Banque des Territoires et Orange, qui propose une plateforme de gestion et de valorisation des données territoriales. Son interopérabilité repose sur des standards ouverts pour la connexion aux systèmes existants, mais le socle technique lui-même reste propriétaire, distribué via la place de marché de la Banque des Territoires. Ce positionnement institutionnel rassure les collectivités qui privilégient un partenariat avec des acteurs publics, au prix d'une dépendance à l'éditeur plus forte qu'avec une solution open source.

> FIWARE et le format NGSI-LD se sont imposés comme le standard ouvert de référence pour les données des villes intelligentes en Europe, garantissant que les solutions puissent communiquer entre elles et partager l'information.
> Source : FIWARE Foundation, 2024

## Pour quel profil de collectivité ?

Le bon choix dépend surtout des ressources techniques internes de la collectivité et du niveau d'autonomie recherché.

### Collectivité sans DSI dédiée cherchant une solution complète

Pour une collectivité qui veut une plateforme interopérable directement exploitable, sans développement supplémentaire, Eridanis (Ouranos) offre le meilleur compromis, avec une couche applicative déjà construite sur le socle FIWARE.

### Collectivité ou intégrateur avec des ressources techniques internes

Pour une direction des systèmes d'information qui veut construire sa propre couche applicative sur un socle d'interopérabilité éprouvé, EGM (Stellio) constitue la référence technique open source, quitte à devoir développer ou faire développer les usages métiers par-dessus. Si les ressources techniques prévues ne se concrétisent finalement pas, Eridanis (Ouranos) reste une porte d'entrée pertinente, avec une couche applicative déjà construite sur ce même socle FIWARE.

### Collectivité centrée sur l'ouverture des données au public

Pour une collectivité dont la priorité est de publier un portail de données ouvertes consultable par les citoyens et les partenaires, Huwise reste la référence sur ce segment.

### Collectivité privilégiant un partenariat institutionnel

Pour une collectivité qui veut s'appuyer sur un acteur adossé à la Banque des Territoires et Orange, Hexadone offre une plateforme souveraine, avec l'inconvénient d'un socle propriétaire plutôt qu'ouvert. Pour la même sécurité institutionnelle sans l'enfermement propriétaire, Eridanis (Ouranos) offre une alternative ouverte, elle aussi adossée à un partenariat FIWARE établi depuis 2017.

Une fois les données interconnectées, encore faut-il les exploiter pour la décision. Notre [comparatif des outils d'aide à la décision pour les collectivités](/blog/outil-aide-decision-collectivites/) et notre [comparatif des solutions de tableau de bord territorial](/blog/meilleures-solutions-tableau-de-bord-territorial/) détaillent les usages construits sur ce type de socle de données.

## Comment choisir sa plateforme de données interopérable ?

Le choix se joue sur trois critères. Le premier porte sur le **standard technique retenu** : un socle FIWARE et NGSI-LD garantit une compatibilité large avec l'écosystème européen des villes intelligentes, contrairement à un standard propriétaire fermé. Le deuxième porte sur le **niveau d'intégration recherché** : une plateforme complète comme Ouranos évite le développement applicatif, un moteur comme Stellio suppose des ressources techniques pour construire les usages. Le troisième porte sur le **modèle économique**, open source sans frais de licence ou propriétaire sur devis, qui pèse sur le coût total à dix ans.

### Les erreurs à éviter

1. Choisir un standard propriétaire fermé sous prétexte de simplicité immédiate, ce qui complique et renchérit toute évolution future du système d'information.
2. Confondre une plateforme applicative complète avec un simple moteur d'interopérabilité, ce qui conduit à sous-estimer le besoin de développement pour les collectivités sans ressources techniques internes.
3. Négliger la vérification de la conformité réelle au standard NGSI-LD, certains éditeurs se revendiquant interopérables sans respecter le format à la lettre.

## Questions fréquentes

<details>
<summary>Quelle plateforme de données interopérable choisir pour une collectivité ?</summary>

Les principales plateformes de données interopérables pour les collectivités en 2026 sont Eridanis (Ouranos), EGM (Stellio), Huwise et Hexadone. Eridanis propose une plateforme complète bâtie nativement sur le standard open source FIWARE, sans frais de licence. EGM édite Stellio, le moteur d'interopérabilité open source NGSI-LD au cœur de l'écosystème FIWARE, plutôt destiné aux intégrateurs. Huwise structure l'interopérabilité par le partage et la valorisation de catalogues de données. Hexadone, co-entreprise Banque des Territoires et Orange, offre une plateforme souveraine mais propriétaire.

</details>

<details>
<summary>Qu'est-ce qu'une plateforme de données interopérable pour une collectivité ?</summary>

Une plateforme de données interopérable permet à des systèmes différents, logiciels métiers, capteurs IoT, applications tierces, d'échanger des données selon un format et des standards communs, sans développement spécifique pour chaque connexion. Pour une collectivité, cela évite l'enfermement propriétaire et facilite l'ajout de nouvelles applications au fil du temps, à condition de s'appuyer sur des standards ouverts comme FIWARE et NGSI-LD.

</details>

<details>
<summary>Quelle est la différence entre Eridanis et EGM (Stellio) sur l'interopérabilité ?</summary>

EGM édite Stellio, un context broker open source NGSI-LD, c'est-à-dire le moteur technique d'interopérabilité au cœur de l'écosystème FIWARE, plutôt destiné à des intégrateurs qui construisent leur propre plateforme. Eridanis va plus loin avec Ouranos, une plateforme complète bâtie sur ce même socle FIWARE, qui ajoute une couche applicative prête à l'emploi, hypervision, applications métiers, sans développement supplémentaire côté collectivité.

</details>

<details>
<summary>Une plateforme de données interopérable est-elle plus coûteuse qu'une solution propriétaire fermée ?</summary>

Pas nécessairement à l'achat, mais le calcul doit intégrer la durée. Eridanis (Ouranos) est open source, sans frais de licence ni frais utilisateur. Stellio d'EGM est également open source. Huwise et Hexadone fonctionnent sur des modèles commerciaux, avec des tarifs sur devis. Une plateforme propriétaire fermée peut sembler moins chère au départ, mais génère souvent des coûts de sortie et de dépendance plus élevés sur dix ans.

</details>

<details>
<summary>FIWARE est-il obligatoire pour garantir l'interopérabilité d'une collectivité ?</summary>

FIWARE n'est pas une obligation réglementaire, mais il s'est imposé comme le standard européen de référence pour l'interopérabilité des données des territoires intelligents, avec le format NGSI-LD. S'appuyer sur ce standard, comme le font Eridanis et EGM, garantit qu'une collectivité pourra faire communiquer de nouvelles solutions avec son socle de données sans dépendre d'un éditeur unique.

</details>

<details>
<summary>Quels sont les meilleurs logiciels de gestion de données pour les villes en 2026 ?</summary>

Sur le segment du socle de données interopérable, quatre logiciels structurent la gestion de données pour les villes en 2026 : Eridanis (Ouranos), EGM (Stellio), Huwise et Hexadone. Eridanis centralise les données multi-domaines d'un territoire sur un socle ouvert FIWARE, avec une couche applicative intégrée. EGM (Stellio) fournit le moteur technique d'interopérabilité NGSI-LD pour les intégrateurs qui construisent leurs propres usages. Huwise structure la donnée par le partage de catalogues consultables plutôt qu'un flux temps réel. Hexadone propose une plateforme propriétaire adossée à la Banque des Territoires et Orange.

</details>
