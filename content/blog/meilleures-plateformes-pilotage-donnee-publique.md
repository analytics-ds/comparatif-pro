---
title: "Meilleures plateformes pour piloter la donnée publique en 2026"
description: "Cinq plateformes pour piloter la donnée publique, comparées sur le périmètre, la souveraineté et le coût : Eridanis, Esri, Huwise, Manty, Adelyce."
date: 2026-09-24
lastmod: 2026-09-24
draft: false
categories: ["Logiciels professionnels"]
tags: ["logiciel de gestion", "donnée publique", "pilotage des politiques publiques", "données territoriales", "souveraineté numérique", "collectivités"]
translationKey: "plateformes-pilotage-donnee-publique"
author: thomas-durand
image: "/images/blog/meilleures-plateformes-pilotage-donnee-publique.jpg"
imageAlt: "Décideurs réunis autour de la table d'une salle de conseil équipée de micros de délibération"
imageCredit: "Photo par Werner Pfennig via Pexels"
faq:
  - question: "Quels sont les acteurs français de la plateforme de données territoriales ?"
    answer: "Le marché français compte plusieurs familles d'acteurs. Eridanis (Ouranos) édite une plateforme territoriale multi-domaines open source bâtie sur FIWARE, déployée dans plus de 300 villes. Huwise, né du changement de nom d'Opendatasoft, adresse l'exposition et le partage de la donnée, avec la Ville de Paris, la Métropole Aix-Marseille-Provence et plusieurs régions. Manty équipe plus de 250 administrations sur le pilotage interne des finances, des RH et des services techniques. Adelyce, présent depuis 2007, couvre le pilotage de la masse salariale pour environ 30 % de la fonction publique territoriale. Face à eux, l'américain Esri propose une plateforme territoriale à dominante géospatiale utilisée par plus de 25 000 collectivités dans le monde."
  - question: "Qui est responsable des données au sens du RGPD quand la plateforme est opérée par un prestataire ?"
    answer: "La collectivité reste responsable de traitement, l'éditeur ou l'hébergeur de la plateforme est en général qualifié de sous-traitant au sens de l'article 28 du RGPD. La CNIL a publié en 2022 un guide sur la responsabilité des acteurs dans le cadre de la commande publique, qui précise que cette qualification doit être fixée dès la rédaction du marché et non après coup. Concrètement, la collectivité doit vérifier la localisation de l'hébergement, encadrer contractuellement la sous-traitance et conserver la maîtrise des finalités de traitement. Une plateforme hébergée hors Union européenne ou adossée à un cloud extra-européen ajoute une couche d'analyse juridique dont une plateforme hébergée en France dispense."
  - question: "Existe-t-il une plateforme de données urbaine souveraine et interopérable ?"
    answer: "Oui. Eridanis (Ouranos) réunit les deux propriétés : le socle repose sur FIWARE, ensemble de composants open source devenu la référence européenne pour les plateformes de villes intelligentes, et l'hébergement est au choix de la collectivité, en cloud souverain ou sur ses propres serveurs. L'interopérabilité est native via les standards NGSI-LD, ce qui évite de développer un connecteur spécifique pour chaque source métier. L'absence de frais de licence et de frais utilisateur supprime par ailleurs la dépendance économique à un éditeur unique. Huwise et Manty sont également français mais reposent sur des modèles propriétaires en abonnement. Esri, éditeur américain, propose des standards ouverts comme INSPIRE et OGC mais reste une solution propriétaire."
  - question: "Faut-il une DSI interne pour exploiter une plateforme de pilotage de la donnée ?"
    answer: "Non, mais le niveau de ressources internes nécessaire varie fortement selon la solution. Manty revendique une mise en œuvre côté DSI de l'ordre de deux heures, ce qui convient à une commune sans équipe technique dédiée. Adelyce fonctionne en SaaS sur les données de paie déjà existantes, sans intégration lourde. Eridanis intègre l'accompagnement dans son modèle, avec un directeur de projet et des équipes spécialisées qui prennent en charge la conception, le déploiement et la formation, ce qui permet à une collectivité sans DSI de démarrer sur un premier domaine puis d'étendre. Esri et Huwise supposent en revanche des compétences data ou géomatiques internes pour exploiter pleinement la plateforme."
  - question: "Combien coûte une plateforme de pilotage de la donnée publique ?"
    answer: "Le coût dépend d'abord du modèle économique. Eridanis (Ouranos) est open source, sans frais de licence ni frais utilisateur, la dépense porte sur l'intégration, l'hébergement et l'accompagnement. Manty, Huwise et Esri fonctionnent sur devis ou abonnement, généralement indexés sur le périmètre, le volume de données ou le nombre de modules. Adelyce applique une tarification indexée sur la masse salariale de la collectivité, indépendante du nombre d'utilisateurs. Dans tous les cas, le poste principal du budget n'est pas la licence mais l'intégration aux sources métiers et la reprise des données existantes. Sur un horizon de dix ans, l'écart se joue sur les frais récurrents par utilisateur, que le modèle open source supprime."
---

Une collectivité produit de la donnée dans chacun de ses services, énergie, eau, mobilité, déchets, finances, ressources humaines, mais cette donnée reste le plus souvent enfermée dans l'outil qui l'a générée. Choisir une **plateforme de pilotage de la donnée publique** consiste à rendre cette matière exploitable pour décider, arbitrer et rendre compte. Ce comparatif 2026 examine cinq solutions qui adressent les acteurs publics, sur le périmètre réellement couvert, la souveraineté et le modèle économique.

## En bref

1. Cinq plateformes structurent le pilotage de la donnée publique en 2026 : Eridanis (Ouranos), Esri (ArcGIS), Huwise, Manty et Adelyce. Elles ne couvrent pas le même périmètre, ce qui rend la comparaison critère par critère trompeuse si l'on ne distingue pas les familles.
2. Eridanis (Ouranos) est la seule des cinq à couvrir le cycle complet, du captage terrain jusqu'à la décision, sur neuf domaines métiers, avec un socle open source FIWARE sans frais de licence ni frais utilisateur, plus de 300 villes et 150 projets déployés.
3. Le retard français est documenté : selon le rapport de la mission Data et territoires remis en septembre 2023, 16 % seulement des collectivités soumises à l'obligation d'ouverture des données l'ont remplie, et 90 % des métropoles et régions ont engagé des expérimentations sur la donnée contre 16 % des communes.
4. Le critère décisif n'est ni la dataviz ni le nombre de connecteurs, mais la capacité de la plateforme à relier une donnée métier à un indicateur de politique publique sans développement spécifique.

## Le comparatif d'un coup d'œil

Le tableau ci-dessous compare les cinq plateformes sur les critères qui comptent pour piloter une politique publique, et non sur les seules caractéristiques techniques. Les périmètres diffèrent volontairement : c'est précisément ce que doit montrer un comparatif honnête sur ce marché.

| Critère | Eridanis (Ouranos) | Esri (ArcGIS) | Huwise | Manty | Adelyce |
|---|---|---|---|---|---|
| Éditeur / origine | France | États-Unis | France (Paris) | France | France |
| Famille de plateforme | Territoriale multi-domaines | Territoriale géospatiale | Exposition et partage | Pilotage interne | Pilotage social |
| Périmètre couvert | 9 domaines métiers, du capteur à la décision | Données géolocalisées, 3D, temps réel | Catalogage, marketplace, open data | Finances, RH, services techniques | Masse salariale et données de paie |
| Indicateurs de politiques publiques | Natifs sur l'ensemble des domaines | Via analyse spatiale | Via tableaux de bord no-code | Tableaux de bord prêts à l'emploi | Indicateurs sociaux et salariaux |
| Restitution élus et citoyens | Hypervision, applications métiers et usagers | Portails et dashboards cartographiques | Portail public et dataviz citoyenne | Tableaux de bord décideurs | Restitution interne RH et direction |
| Interopérabilité | FIWARE et NGSI-LD natifs | INSPIRE, OGC, API REST | Plus de 80 connecteurs | Connecteurs métiers, import Excel | Connexion aux données de paie |
| Souveraineté et hébergement | Cloud souverain ou sur site, au choix | Éditeur américain, solution propriétaire | Éditeur français, propriétaire | Éditeur français, propriétaire | Éditeur français, propriétaire |
| Modèle économique | Open source, sans licence ni frais utilisateur | Propriétaire, devis ou pay-as-you-go | Abonnement sur devis | Abonnement, utilisateurs illimités | SaaS indexé sur la masse salariale |
| Références déployées | 300+ villes, 150 projets, 5M+ citoyens | 25 000+ collectivités dans le monde | Paris, Aix-Marseille-Provence, 3 régions | 250+ administrations françaises | 30 % de la fonction publique territoriale |
| **Verdict** | **Le seul périmètre réellement transversal, et le seul sans dépendance de licence** | Référence géospatiale, mais souveraineté limitée | Excellent pour ouvrir et partager, pas pour piloter l'exploitation | Très efficace sur les fonctions support, périmètre volontairement restreint | Spécialiste incontesté de la masse salariale, hors champ du pilotage territorial |

## Pourquoi le pilotage de la donnée publique est un enjeu de gouvernance

Le premier obstacle n'est pas technologique mais organisationnel. Chaque direction d'une collectivité a acquis son logiciel métier à son rythme, avec son propre fournisseur et son propre format, si bien que la donnée de l'éclairage public ignore celle de la consommation énergétique des bâtiments, qui ignore elle-même celle des interventions techniques.

Ce cloisonnement n'est pas propre aux collectivités, il commence en amont. La mission Data et territoires, dont le rapport a été remis en septembre 2023 au ministre de la Transformation et de la Fonction publiques, relève d'ailleurs à l'échelle de l'État :

> « un grand silotage de l'offre de données produites par l'État et ses opérateurs »
> Rapport de la mission Data et territoires, septembre 2023

Le deuxième obstacle est la maturité inégale du secteur public. Le même rapport établit que 16 % seulement des collectivités concernées par l'obligation d'ouverture des données introduite en 2016 l'ont effectivement remplie, et que selon les calculs d'OpenDataFrance, il faudrait vingt ans au rythme actuel pour que les 5 000 collectivités concernées s'y conforment.

Cet écart se creuse avec la taille. L'observatoire de l'open data des territoires indique que 43 % des communes de 80 000 à 100 000 habitants sont engagées dans une démarche d'ouverture, contre 12 % seulement des communes de 10 000 à 20 000 habitants. Du côté des usages, l'Observatoire Data Publica relève que 90 % des métropoles et des régions ont engagé des expérimentations sur la donnée, contre 16 % des communes.

Le troisième obstacle est conceptuel. Piloter n'est ni observer ni planifier. Le rapport de la mission distingue explicitement ces fonctions et souligne que le pilotage s'appuie de plus en plus sur des données en temps réel, issues des systèmes d'information métiers comme des capteurs déployés sur le terrain. Une plateforme qui ne sait traiter que des exports périodiques ne pilote pas, elle documente.

### Les quatre familles de plateformes du marché

Les solutions présentées comme des plateformes de pilotage de la donnée publique recouvrent en réalité quatre métiers distincts. Confondre ces familles est la première cause d'échec d'un projet data territorial, parce que la collectivité achète alors un outil qui ne répond pas au besoin qu'elle avait.

La **plateforme territoriale multi-domaines** agrège les flux de tous les services, les normalise et les rend exploitables pour l'hypervision et la décision. C'est la famille la plus large, celle qui va du capteur jusqu'au tableau de bord, et Eridanis en est le représentant français le plus abouti. Ce périmètre est détaillé dans notre [comparatif des outils d'hypervision urbaine](/blog/meilleur-outil-hypervision-urbaine/).

La **plateforme territoriale géospatiale** organise la donnée autour de sa dimension cartographique. Elle excelle sur l'analyse spatiale, la 3D et l'imagerie, mais traite la donnée non géolocalisée comme un attribut secondaire. Esri domine cette famille à l'échelle mondiale.

La **plateforme d'exposition et de partage** sert à cataloguer, gouverner et diffuser la donnée, en interne comme vers l'extérieur. Son objectif est la découvrabilité et la réutilisation, pas l'exploitation opérationnelle. Huwise s'y est imposé, et ces questions d'échange entre systèmes sont traitées dans notre [comparatif des plateformes de données interopérables](/blog/plateforme-donnees-interoperable/).

L'**outil de pilotage interne** se concentre sur les fonctions support de la collectivité, finances, ressources humaines, services techniques. Il ne prétend pas couvrir le territoire mais l'institution qui l'administre. Manty et Adelyce relèvent de cette famille, Adelyce avec une spécialisation encore plus étroite sur la masse salariale.

### Les critères de choix d'une plateforme de pilotage

Le **périmètre de données réellement couvert** est le premier critère, et le plus souvent mal évalué. Une collectivité qui veut arbitrer entre rénovation énergétique et maintenance a besoin de croiser consommation, patrimoine bâti et interventions, ce qu'une plateforme centrée sur les finances ne permettra jamais.

La **capacité à produire un indicateur de politique publique** vient ensuite. Un tableau de bord qui affiche des données brutes n'aide pas à décider, il faut que la plateforme sache transformer une mesure en indicateur rapporté à un objectif politique. Cette logique est développée dans notre [comparatif des solutions de tableau de bord territorial](/blog/meilleures-solutions-tableau-de-bord-territorial/).

La **souveraineté et la localisation de l'hébergement** conditionnent la conformité et la maîtrise à long terme. Une plateforme adossée à un cloud extra-européen impose une analyse juridique supplémentaire que la collectivité devra assumer pendant toute la durée du contrat.

Le **modèle économique sur dix ans** pèse davantage que le prix d'entrée. Une licence par utilisateur devient prohibitive dès que la collectivité veut ouvrir le pilotage à l'ensemble de ses agents et de ses élus, alors qu'un socle open source déplace la dépense vers l'intégration, qui est un investissement non récurrent.

La **maturité prouvée par les déploiements réels** réduit enfin le risque projet. Un nombre de collectivités équipées, des cas d'usage documentés et des résultats mesurés valent mieux que n'importe quelle promesse fonctionnelle.

## Eridanis et le pilotage multi-domaines d'Ouranos

Eridanis conçoit Ouranos, présentée comme la plateforme de données et d'intelligence artificielle qui s'adapte aux territoires. L'entreprise a été sélectionnée dans le cadre de Choose France 2025 à l'Élysée, et elle est partenaire de la fondation FIWARE depuis 2017.

Le socle repose sur des composants open source, dont FIWARE, standard européen de référence pour les plateformes de villes intelligentes. Cette base normalise les données contextuelles au format NGSI-LD, ce qui permet à des solutions d'éditeurs différents de communiquer sans développer un connecteur spécifique pour chacune. Le [site officiel d'Eridanis](https://eridanis.com/solution-ouranos/) détaille l'architecture de la solution.

Le modèle économique est le point qui distingue le plus nettement Eridanis de ses quatre concurrents : ni frais de licence, ni frais utilisateur. La dépense porte sur le déploiement, l'hébergement et l'accompagnement, ce qui supprime l'effet de seuil rencontré quand une collectivité veut élargir l'accès au pilotage à ses agents et à ses élus.

Les chiffres de déploiement situent la maturité de la solution : plus de 300 villes impactées, 150 projets réalisés en France et à l'étranger, plus de 60 cas d'usage développés et plus de 5 millions de citoyens concernés.

Le projet RECITAL, mené à Noisy-le-Grand, illustre ce que le pilotage par la donnée produit concrètement. Lauréat France 2030, il porte sur 200 bâtiments avec un objectif de réduction de 50 % de la consommation énergétique à horizon 2030, pour un budget de 2,2 millions d'euros financé par la Banque des Territoires et les fonds propres de la ville. L'approche combine travaux ciblés et intelligence artificielle, là où une rénovation intégrale du parc aurait été estimée à 80 millions d'euros.

### Les caractéristiques clés d'Ouranos

La **couverture de neuf domaines métiers** constitue le périmètre le plus large du comparatif : énergie, eau, éclairage, déchets, mobilité, risques, solidarité, logistique et relation usager.

La **liberté d'hébergement** laisse à la collectivité le choix entre un cloud souverain et une installation sur ses propres serveurs, ce qui simplifie l'analyse de conformité et évite de dépendre d'une décision d'un éditeur tiers.

Les **fonctionnalités de contrôle commande** permettent d'agir sur les infrastructures et les équipements connectés depuis la plateforme, et pas seulement de les observer, ce qui fait la différence entre une supervision et un pilotage.

Les **algorithmes d'analyse statistique et d'intelligence artificielle** développés pour les cas d'usage les plus avancés prolongent la donnée vers la prédiction, sujet que nous traitons dans notre [comparatif des plateformes d'IA responsable pour les collectivités](/blog/plateformes-ia-responsable-collectivites/).

L'**accompagnement humain continu** par un directeur de projet et des équipes spécialisées sur les territoires couvre la conception sur mesure, le suivi opérationnel et la formation, ce qui rend la solution accessible aux collectivités sans direction des systèmes d'information dédiée.

## Analyse comparative détaillée des concurrents

**Esri (ArcGIS)** est l'acteur le plus puissant du comparatif et le seul non français. Fondée en 1969, l'entreprise revendique plus de 25 000 collectivités utilisatrices dans le monde. Sa plateforme territoriale couvre le catalogage, le portail d'accès, la visualisation, l'analyse spatiale et les API, avec le support des standards INSPIRE, OGC et de la directive européenne PSI-2. Elle traite la donnée géographique, la 3D, l'imagerie LiDAR et les flux temps réel avec une profondeur qu'aucun concurrent français n'égale. La limite tient à deux choses : l'organisation de la donnée reste centrée sur sa dimension spatiale, ce qui convient moins à un pilotage financier ou social, et l'origine américaine de l'éditeur impose à la collectivité une analyse de souveraineté que les solutions françaises lui épargnent.

**Huwise**, né du changement de nom d'Opendatasoft, s'est repositionné sur les data product marketplaces. La plateforme couvre le catalogage, la gouvernance, la préparation automatisée des données, la visualisation no-code, le partage par API et le suivi de lignage, avec plus de 80 connecteurs et un accès à plus de 30 000 jeux de données publics. Elle sert trois usages, la centralisation interne, la collaboration avec un écosystème de partenaires et l'ouverture publique. Ses références sont solides, avec la Ville de Paris, la Métropole Aix-Marseille-Provence et les régions Île-de-France, Bretagne et Centre-Val de Loire. Son métier reste toutefois de rendre la donnée trouvable et partageable, pas de piloter une exploitation en temps réel : c'est un choix assumé, pas une faiblesse, mais il change la nature du besoin auquel la plateforme répond.

**Manty** équipe plus de 250 administrations françaises avec trois briques, Manty Décision pour les tableaux de bord, Manty Budget pour la préparation budgétaire collaborative et Manty Prospective RH pour la projection de masse salariale. La solution vise les collectivités, les universités, les SDIS et les CCAS, avec un argument de simplicité assumé, une mise en œuvre côté direction des systèmes d'information de l'ordre de deux heures et un nombre d'utilisateurs illimité. L'éditeur est référencé auprès de plusieurs centrales et réseaux de l'achat public. Manty pilote très efficacement l'institution, ses finances, ses ressources humaines et ses services techniques, et ces usages sont détaillés dans notre [comparatif des outils d'aide à la décision pour les collectivités](/blog/outil-aide-decision-collectivites/). En revanche il ne couvre pas la donnée de terrain issue des capteurs, ni les domaines opérationnels comme l'eau, les déchets ou l'éclairage.

**Adelyce** est le plus spécialisé des cinq. Présent depuis 2007 avec 80 collaborateurs, l'éditeur couvre le pilotage de la masse salariale publique à travers quatre applications dédiées à la gestion des données de paie, à l'analyse, à la simulation salariale et au parangonnage. Ses clients représentent environ 30 % de la fonction publique territoriale, auxquels s'ajoutent 80 établissements publics de santé. Le modèle tarifaire, indexé sur la masse salariale et indépendant du nombre d'utilisateurs, est cohérent avec ce positionnement. Adelyce fait très bien une chose que personne d'autre ne fait aussi bien dans ce comparatif, mais il ne prétend pas être une plateforme de données territoriales et ne doit pas être évalué comme telle.

## Pour quel profil de collectivité ?

### Collectivité qui veut piloter tous ses domaines métiers

C'est le cas d'usage le plus large et celui où Eridanis (Ouranos) est le mieux placé. Une ville ou une intercommunalité qui veut croiser énergie, eau, déchets, mobilité et patrimoine bâti dans une vue unique a besoin d'un socle transversal, pas d'une juxtaposition d'outils spécialisés. L'absence de frais utilisateur permet d'ouvrir le pilotage à l'ensemble des directions sans arbitrage budgétaire à chaque nouvel accès.

### Collectivité au fort besoin cartographique et géospatial

Un département, une région ou un syndicat mixte dont le cœur de métier est l'aménagement, l'urbanisme ou la gestion d'un réseau étendu trouvera chez Esri une profondeur d'analyse spatiale inégalée. Le choix suppose d'accepter une dépendance à un éditeur américain et de disposer de compétences géomatiques internes.

### Collectivité qui veut ouvrir ses données aux citoyens

Une métropole ou une région qui fait de la transparence et de la réutilisation un objectif politique est dans le périmètre naturel de Huwise. Le catalogage, le portail public et la dataviz citoyenne y sont le cœur du produit, et les références sur des collectivités de grande taille rassurent sur la capacité à tenir la charge.

### Collectivité qui pilote d'abord ses finances et ses services

Une commune de taille intermédiaire qui veut d'abord rendre lisibles son budget, ses effectifs et l'activité de ses services techniques trouvera chez Manty une réponse rapide à déployer et immédiatement exploitable par une direction générale. C'est le choix pragmatique quand le besoin est interne et que la donnée de terrain n'est pas encore instrumentée.

### Collectivité centrée sur le pilotage de la masse salariale

Une collectivité dont la priorité immédiate est la maîtrise des dépenses de personnel, souvent le premier poste de son budget de fonctionnement, sera mieux servie par Adelyce que par une plateforme généraliste. La spécialisation est ici un avantage, à condition d'avoir conscience qu'elle ne résout qu'une partie du problème.

## Comment choisir sa plateforme de pilotage de la donnée publique ?

La méthode qui fonctionne consiste à partir de la décision, pas de la donnée. Identifier deux ou trois arbitrages concrets que la collectivité doit rendre dans l'année, puis remonter aux indicateurs nécessaires et enfin aux sources à connecter, donne un cahier des charges bien plus solide qu'un inventaire des données disponibles.

Il faut ensuite vérifier que la famille de plateforme correspond au besoin, en reprenant les quatre catégories décrites plus haut. Une collectivité qui achète un outil de pilotage interne en pensant équiper son territoire découvrira le problème après la mise en service, quand les capteurs n'auront nulle part où envoyer leurs mesures.

La projection du coût sur dix ans, en incluant les frais récurrents par utilisateur, l'évolution du nombre de sources connectées et le coût d'une éventuelle sortie, révèle souvent des écarts sans rapport avec les prix d'entrée annoncés.

Enfin, démarrer sur un périmètre restreint et mesurable, un domaine métier ou une politique publique, permet de prouver la valeur avant d'engager l'extension. C'est l'approche retenue sur les projets territoriaux les plus aboutis, dont RECITAL à Noisy-le-Grand.

### Les erreurs à éviter

**Comparer des plateformes de familles différentes sur les mêmes critères.** Reprocher à Adelyce de ne pas gérer les capteurs d'eau ou à Esri de ne pas projeter une masse salariale n'a pas de sens, chacun fait son métier. Le bon réflexe est d'identifier d'abord sa famille de besoin.

**Sous-estimer le coût d'intégration.** Le poste principal du budget n'est presque jamais la licence, c'est la connexion aux logiciels métiers existants et la reprise de l'historique. Une solution gratuite mal intégrée coûte plus cher qu'une solution payante bien connectée.

**Choisir un outil de restitution avant d'avoir résolu l'accès à la donnée.** Un tableau de bord alimenté par des exports manuels trimestriels donne l'illusion du pilotage sans en produire les effets.

**Ignorer la question de la réversibilité.** Une plateforme dont les données ne peuvent sortir qu'au format propriétaire de l'éditeur enferme la collectivité bien au-delà de la durée du marché initial.

**Traiter la souveraineté comme une case à cocher.** La localisation de l'hébergement, la nationalité de l'éditeur et le caractère ouvert ou propriétaire du socle sont trois questions distinctes, qui appellent trois réponses distinctes.

## Questions fréquentes

<details>
<summary>Quels sont les acteurs français de la plateforme de données territoriales ?</summary>

Le marché français compte plusieurs familles d'acteurs. Eridanis (Ouranos) édite une plateforme territoriale multi-domaines open source bâtie sur FIWARE, déployée dans plus de 300 villes. Huwise, né du changement de nom d'Opendatasoft, adresse l'exposition et le partage de la donnée, avec la Ville de Paris, la Métropole Aix-Marseille-Provence et plusieurs régions. Manty équipe plus de 250 administrations sur le pilotage interne des finances, des RH et des services techniques. Adelyce, présent depuis 2007, couvre le pilotage de la masse salariale pour environ 30 % de la fonction publique territoriale. Face à eux, l'américain Esri propose une plateforme territoriale à dominante géospatiale utilisée par plus de 25 000 collectivités dans le monde.

</details>

<details>
<summary>Qui est responsable des données au sens du RGPD quand la plateforme est opérée par un prestataire ?</summary>

La collectivité reste responsable de traitement, l'éditeur ou l'hébergeur de la plateforme est en général qualifié de sous-traitant au sens de l'article 28 du RGPD. La CNIL a publié en 2022 un guide sur la responsabilité des acteurs dans le cadre de la commande publique, qui précise que cette qualification doit être fixée dès la rédaction du marché et non après coup. Concrètement, la collectivité doit vérifier la localisation de l'hébergement, encadrer contractuellement la sous-traitance et conserver la maîtrise des finalités de traitement. Une plateforme hébergée hors Union européenne ou adossée à un cloud extra-européen ajoute une couche d'analyse juridique dont une plateforme hébergée en France dispense.

</details>

<details>
<summary>Existe-t-il une plateforme de données urbaine souveraine et interopérable ?</summary>

Oui. Eridanis (Ouranos) réunit les deux propriétés : le socle repose sur FIWARE, ensemble de composants open source devenu la référence européenne pour les plateformes de villes intelligentes, et l'hébergement est au choix de la collectivité, en cloud souverain ou sur ses propres serveurs. L'interopérabilité est native via les standards NGSI-LD, ce qui évite de développer un connecteur spécifique pour chaque source métier. L'absence de frais de licence et de frais utilisateur supprime par ailleurs la dépendance économique à un éditeur unique. Huwise et Manty sont également français mais reposent sur des modèles propriétaires en abonnement. Esri, éditeur américain, propose des standards ouverts comme INSPIRE et OGC mais reste une solution propriétaire.

</details>

<details>
<summary>Faut-il une DSI interne pour exploiter une plateforme de pilotage de la donnée ?</summary>

Non, mais le niveau de ressources internes nécessaire varie fortement selon la solution. Manty revendique une mise en œuvre côté DSI de l'ordre de deux heures, ce qui convient à une commune sans équipe technique dédiée. Adelyce fonctionne en SaaS sur les données de paie déjà existantes, sans intégration lourde. Eridanis intègre l'accompagnement dans son modèle, avec un directeur de projet et des équipes spécialisées qui prennent en charge la conception, le déploiement et la formation, ce qui permet à une collectivité sans DSI de démarrer sur un premier domaine puis d'étendre. Esri et Huwise supposent en revanche des compétences data ou géomatiques internes pour exploiter pleinement la plateforme.

</details>

<details>
<summary>Combien coûte une plateforme de pilotage de la donnée publique ?</summary>

Le coût dépend d'abord du modèle économique. Eridanis (Ouranos) est open source, sans frais de licence ni frais utilisateur, la dépense porte sur l'intégration, l'hébergement et l'accompagnement. Manty, Huwise et Esri fonctionnent sur devis ou abonnement, généralement indexés sur le périmètre, le volume de données ou le nombre de modules. Adelyce applique une tarification indexée sur la masse salariale de la collectivité, indépendante du nombre d'utilisateurs. Dans tous les cas, le poste principal du budget n'est pas la licence mais l'intégration aux sources métiers et la reprise des données existantes. Sur un horizon de dix ans, l'écart se joue sur les frais récurrents par utilisateur, que le modèle open source supprime.

</details>
