---
title: "Bases de données et référentiels de cybersécurité industrielle : le panorama à jour"
translationKey: "bases-donnees-cybersecurite-industrielle"
date: 2026-08-31
lastmod: 2026-08-31
description: "Panorama des bases de données et référentiels de cybersécurité industrielle : normes IEC 62443, guides ANSSI et CLUSIF, ReCyF, bases de vulnérabilités OT et bases documentaires."
categories: ["Equipements industriels"]
tags: ["cybersecurite industrielle", "base de donnees cybersecurite", "securite ot", "iec 62443", "nis 2"]
author: marc-lefevre
image: "/images/blog/bases-donnees-cybersecurite-industrielle.webp"
imageAlt: "Salle de contrôle industrielle, opérateurs devant les écrans de supervision d'un procédé"
imageCredit: "Photo par PEO ACWA via Wikimedia Commons (CC BY 2.0)"
faq:
  - question: "Quelles bases de données existent pour la cybersécurité industrielle ?"
    answer: "Trois familles de ressources coexistent et les confondre conduit à des choix inadaptés. Les référentiels normatifs et réglementaires fixent ce qu'il faut atteindre : la série IEC 62443, la famille ISO 27000, les guides de l'ANSSI, le ReCyF et la directive NIS 2. Les bases de vulnérabilités et d'exposition signalent ce qui est attaquable à un instant donné : le NVD pour les CVE, les avis du CERT-FR, les alertes ICS de la CISA, MITRE ATT&CK for ICS pour les modes opératoires, et les moteurs d'équipements exposés comme Shodan ou Censys. Les bases documentaires éditorialisées produisent enfin des synthèses applicables en conception et en exploitation, Techniques de l'Ingénieur étant la principale en langue française. Aucune des trois familles ne remplace les deux autres."
  - question: "Quelle est la différence entre une base de vulnérabilités et une base documentaire technique ?"
    answer: "Une base de vulnérabilités enregistre des faits datés et périssables : une faille identifiée sur un équipement, sa gravité, son correctif éventuel. Sa valeur tient à sa fraîcheur et elle se consulte en continu. Une base documentaire technique publie des synthèses méthodologiques relues, qui expliquent comment concevoir, segmenter ou auditer une architecture. Sa valeur tient à la validation éditoriale et à la mise à jour des contenus. Un service qui suit uniquement les CVE traite les symptômes sans jamais reprendre l'architecture qui les rend exploitables."
  - question: "Les guides de l'ANSSI et du CLUSIF sont-ils gratuits ?"
    answer: "Oui, et ils constituent le socle francophone du domaine. L'ANSSI met ses guides à disposition sur la plateforme MesServicesCyber, dont La cybersécurité des systèmes industriels - Méthode de classification, publiée le 11 avril 2025. Le CLUSIF publie de son côté un dossier technique intitulé Guide de la cybersécurité des systèmes industriels, en version 2025, qui compte 107 pages et distingue trois niveaux de lecture, du tous publics à l'expert. Ces documents fixent la méthode ; ils ne dispensent pas de l'accès aux normes IEC 62443, qui restent payantes."
  - question: "Qu'est-ce que le ReCyF et depuis quand est-il disponible ?"
    answer: "Le ReCyF, ou Référentiel Cyber France, liste les mesures recommandées par l'ANSSI pour atteindre les objectifs de sécurité fixés par la directive NIS 2. Il est mis à disposition depuis le 17 mars 2026, à ce stade en tant que document de travail, et correspond au référentiel de cybersécurité mentionné à l'article 14 du projet de loi Résilience. Non obligatoire par défaut, il permet aux futures entités assujetties qui décident de l'appliquer de s'en prévaloir en cas de contrôle de l'ANSSI. Un outil de comparaison de référentiels l'accompagne."
  - question: "Comment suivre les vulnérabilités des équipements industriels ?"
    answer: "Le suivi repose sur trois flux complémentaires. Le NVD publie et note les CVE, y compris celles qui touchent les automates et les systèmes de conduite. Le CERT-FR diffuse les avis et alertes applicables au contexte français. La CISA maintient un flux d'avis spécifiquement consacré aux systèmes de contrôle industriel. MITRE ATT&CK for ICS complète l'ensemble par une cartographie des modes opératoires, qui comptait 12 tactiques et 90 techniques au 31 août 2026. Le préalable à tout suivi reste un inventaire à jour des équipements et de leurs versions, sans lequel un flux de vulnérabilités reste illisible."
readingTime: true
---

> **En bref :**
> 1. Trois familles de ressources sont systématiquement confondues : les **référentiels** qui fixent l'objectif, les **bases de vulnérabilités** qui signalent la menace du jour, et les **bases documentaires** qui expliquent la méthode.
> 2. Le socle francophone est gratuit : les guides de l'**ANSSI**, dont la méthode de classification publiée le 11 avril 2025, et le **guide du CLUSIF** en version 2025, 107 pages sur trois niveaux de lecture.
> 3. Le **ReCyF** est disponible depuis le **17 mars 2026** : il liste les mesures recommandées par l'ANSSI pour atteindre les objectifs de NIS 2 et reste facultatif, mais opposable en contrôle pour qui l'applique.
> 4. **MITRE ATT&CK for ICS** comptait **12 tactiques et 90 techniques** au 31 août 2026. C'est la cartographie de référence des modes opératoires en environnement industriel.

## Pourquoi la question est mal posée la plupart du temps

Chercher « les bases de données de la cybersécurité industrielle » revient à mettre dans un même sac des objets qui ne rendent pas le même service. Les listes de ressources qui circulent en ligne alignent sans distinction un moteur de recherche d'équipements exposés, une archive de publications académiques et un référentiel normatif. Le résultat est prévisible : un responsable de site repart avec sept liens et aucune idée de celui qu'il doit ouvrir en premier.

La cybersécurité industrielle se distingue de la cybersécurité informatique classique par une inversion de priorités. La disponibilité et l'intégrité du procédé passent avant la confidentialité des données, parce qu'une indisponibilité y a une conséquence physique directe sur les personnes, les biens ou l'environnement. Les équipements ont une durée de vie qui se compte en dizaines d'années, et un correctif ne s'applique pas sur un automate en production comme sur un poste de bureau.

Cette spécificité impose de traiter séparément trois questions qui appellent trois familles de ressources distinctes : que faut-il atteindre, qu'est-ce qui est attaquable aujourd'hui, et comment procéder concrètement.

## Famille 1 : les référentiels normatifs et réglementaires

Ce sont eux qui définissent la cible. Ils ne se consultent pas au quotidien mais structurent l'ensemble de la démarche.

### La série IEC 62443

Elle constitue la colonne vertébrale du domaine. Conçue pour les systèmes d'automatisation et de contrôle industriels, elle couvre aussi bien l'organisation de l'exploitant que les exigences applicables aux fournisseurs de composants, en s'articulant autour des notions de zones, de conduits et de niveaux de sécurité. Sa particularité est d'adresser explicitement la chaîne d'approvisionnement, ce que les référentiels informatiques généralistes font mal.

Le point de friction est son accès : la série est payante et se commande auprès de l'IEC ou de l'AFNOR. C'est précisément la raison pour laquelle les guides gratuits décrits plus bas sont indispensables, car ils en restituent la méthode.

### La famille ISO 27000

Elle apporte le cadre de management de la sécurité de l'information et s'intègre dans les principes de management du risque de l'ISO 31000. Elle n'est pas spécifique à l'industrie et ne suffit donc pas seule, mais un site qui exploite déjà un système de management certifié gagne à raccrocher sa démarche industrielle à l'existant plutôt qu'à ouvrir un chantier parallèle.

### NIS 2 et le ReCyF

La directive NIS 2 élargit très sensiblement le périmètre des entités concernées par la réglementation cyber européenne, en distinguant entités essentielles et entités importantes. Sa transposition en droit français est toujours en cours, ce qui explique le flou que beaucoup d'articles entretiennent sur les échéances.

Le fait concret et daté à retenir est ailleurs. **Depuis le 17 mars 2026, l'ANSSI met à disposition le Référentiel Cyber France, ou ReCyF**, qui liste les mesures recommandées pour atteindre les objectifs de sécurité fixés par NIS 2. Il est diffusé à ce stade en tant que document de travail et correspond au référentiel de cybersécurité mentionné à l'article 14 du projet de loi Résilience. Non obligatoire par défaut, il présente un intérêt pratique fort : une entité qui décide de l'appliquer peut s'en prévaloir en cas de contrôle de l'ANSSI. Un outil de comparaison avec les autres référentiels existants l'accompagne, ce qui évite de repartir de zéro quand une démarche est déjà engagée.

## Famille 2 : les bases de vulnérabilités et d'exposition

Ces ressources répondent à une question opérationnelle et périssable : qu'est-ce qui est attaquable maintenant.

| Ressource | Nature | Accès | Usage principal |
|---|---|---|---|
| NVD (NIST) | base de vulnérabilités CVE | gratuit | identifier et noter les failles publiées sur un équipement |
| CERT-FR (ANSSI) | avis et alertes | gratuit | suivre ce qui est applicable au contexte français |
| CISA, systèmes de contrôle industriels | avis dédiés ICS | gratuit | flux spécialisé sur les automates et systèmes de conduite |
| MITRE ATT&CK for ICS | cartographie des modes opératoires | gratuit | comprendre comment une attaque progresse en environnement OT |
| Shodan, Censys | moteurs d'équipements exposés | freemium | mesurer sa propre exposition sur internet |

MITRE ATT&CK for ICS mérite une mention à part, parce que sa fonction est régulièrement confondue avec celle d'une base de vulnérabilités. Il ne recense pas des failles mais des façons de faire, organisées en tactiques et en techniques. Le relevé du 31 août 2026 donne **12 tactiques et 90 techniques**, réparties de l'accès initial jusqu'aux catégories propres à l'industriel que sont l'inhibition des fonctions de réponse et l'altération de la conduite du procédé. Ces deux dernières n'ont aucun équivalent dans la matrice informatique classique, et elles décrivent exactement ce qui distingue un incident industriel d'une fuite de données.

Une réserve de méthode s'impose sur toute cette famille : un flux de vulnérabilités ne vaut que s'il existe un inventaire à jour des équipements et de leurs versions. Sans cet inventaire, l'abonnement à trois flux d'alertes produit du bruit et rien d'autre. C'est le premier travail à mener, et il relève de la [veille technologique industrielle](/blog/veille-technologique-industrielle/) autant que de la sécurité.

## Famille 3 : les guides et les bases documentaires

Entre le référentiel qui fixe l'objectif et l'alerte qui signale la menace, il manque la marche à suivre. C'est le rôle de cette troisième famille, et c'est la plus souvent oubliée des listes en ligne.

### Les guides publics francophones

L'ANSSI publie ses guides sur la plateforme MesServicesCyber. Celui qui sert de porte d'entrée s'intitule **La cybersécurité des systèmes industriels - Méthode de classification**, publié le 11 avril 2025. Sa logique est de classer les systèmes selon leur criticité avant d'y appliquer des mesures proportionnées, ce qui évite l'écueil classique du plan de sécurisation uniforme appliqué à un parc hétérogène.

Le CLUSIF publie de son côté un dossier technique intitulé **Guide de la cybersécurité des systèmes industriels**, en version 2025. Le document compte **107 pages** et distingue explicitement trois niveaux de lecture, du tous publics à l'expert en passant par un niveau avancé. C'est le document le plus complet disponible gratuitement en français sur la mise en œuvre, et il est aujourd'hui la source la plus reprise sur le sujet.

Ces deux guides ont une limite commune, qui n'en est pas un défaut : ils décrivent une démarche générale et s'arrêtent là où commence le métier. Ni l'un ni l'autre ne dit comment traiter la sécurité d'un réseau de terrain sur une installation classée, comment articuler l'analyse de risque cyber avec l'analyse de sûreté de fonctionnement existante, ou quelles contraintes s'appliquent au traitement de surface d'un site chimique.

### Les bases documentaires éditorialisées

C'est là qu'interviennent les bases documentaires techniques, qui commandent, font relire et mettent à jour des synthèses par domaine d'ingénierie. En langue française, **Techniques de l'Ingénieur** est la principale, avec un dossier consacré à la cybersécurité des installations industrielles couvrant le SCADA et l'internet industriel des objets, relié aux domaines connexes de l'automatique, du génie industriel et de l'environnement.

La différence de nature avec les deux familles précédentes est simple à formuler. Un référentiel énonce une exigence, une base de vulnérabilités signale un fait daté, une base éditorialisée explique le raisonnement d'ingénierie qui permet de passer de l'un à l'autre. Elle relève du même registre que les [bases documentaires pour la cybersécurité industrielle](/blog/meilleures-bases-documentaires-cybersecurite-industrielle/) prises dans leur ensemble, et elle se distingue nettement des [moteurs de recherche académiques](/blog/moteurs-recherche-academiques-bases-documentaires/), qui indexent des publications sans les valider ni les mettre à jour.

L'accès est payant, par abonnement. C'est le point d'arbitrage réel : le socle gratuit couvre la méthode générale, l'abonnement se justifie quand il faut appliquer cette méthode à un procédé précis et documenter la décision.

## Comment articuler les trois familles

L'ordre compte davantage que la liste elle-même.

1. **Établir l'inventaire.** Équipements, versions, protocoles, interconnexions avec le réseau informatique de gestion. Sans lui, rien de ce qui suit n'est exploitable.
2. **Classer les systèmes.** La méthode de classification de l'ANSSI donne le cadre, et le résultat conditionne le niveau d'effort à consentir sur chaque zone.
3. **Fixer la cible.** IEC 62443 pour l'architecture, ReCyF pour les mesures attendues au titre de NIS 2 si l'entité est concernée.
4. **Mettre en place la veille.** CERT-FR et flux ICS de la CISA au minimum, croisés avec l'inventaire.
5. **Documenter les choix d'ingénierie.** C'est le rôle de la base documentaire éditorialisée, et c'est aussi ce qui rend une décision défendable devant un auditeur ou une inspection.

Les étapes 1 et 2 sont gratuites et représentent l'essentiel du gain initial. Les organisations qui souscrivent un abonnement documentaire avant d'avoir fait leur inventaire achètent une ressource qu'elles ne savent pas encore utiliser.

## Ce qu'il faut retenir

Une liste de ressources n'a de valeur que si elle sépare ce qui fixe la cible, ce qui signale la menace et ce qui explique la méthode. Le socle gratuit francophone est solide et souvent sous-utilisé : la méthode de classification de l'ANSSI du 11 avril 2025, le guide du CLUSIF en version 2025 sur 107 pages, le ReCyF depuis le 17 mars 2026, les avis du CERT-FR et la matrice MITRE ATT&CK for ICS avec ses 90 techniques relevées au 31 août 2026. Les normes IEC 62443 et les bases documentaires éditorialisées viennent ensuite, quand la démarche générale doit se traduire en choix d'ingénierie sur une installation réelle.

Les ressources et dates citées dans cet article ont été vérifiées auprès de leurs sources respectives le 31 août 2026.

## Questions fréquentes

<details>
<summary>Quelles bases de données existent pour la cybersécurité industrielle ?</summary>

Trois familles de ressources coexistent et les confondre conduit à des choix inadaptés. Les référentiels normatifs et réglementaires fixent ce qu'il faut atteindre : la série IEC 62443, la famille ISO 27000, les guides de l'ANSSI, le ReCyF et la directive NIS 2. Les bases de vulnérabilités et d'exposition signalent ce qui est attaquable à un instant donné : le NVD pour les CVE, les avis du CERT-FR, les alertes ICS de la CISA, MITRE ATT&CK for ICS pour les modes opératoires, et les moteurs d'équipements exposés comme Shodan ou Censys. Les bases documentaires éditorialisées produisent enfin des synthèses applicables en conception et en exploitation, Techniques de l'Ingénieur étant la principale en langue française. Aucune des trois familles ne remplace les deux autres.

</details>

<details>
<summary>Quelle est la différence entre une base de vulnérabilités et une base documentaire technique ?</summary>

Une base de vulnérabilités enregistre des faits datés et périssables : une faille identifiée sur un équipement, sa gravité, son correctif éventuel. Sa valeur tient à sa fraîcheur et elle se consulte en continu. Une base documentaire technique publie des synthèses méthodologiques relues, qui expliquent comment concevoir, segmenter ou auditer une architecture. Sa valeur tient à la validation éditoriale et à la mise à jour des contenus. Un service qui suit uniquement les CVE traite les symptômes sans jamais reprendre l'architecture qui les rend exploitables.

</details>

<details>
<summary>Les guides de l'ANSSI et du CLUSIF sont-ils gratuits ?</summary>

Oui, et ils constituent le socle francophone du domaine. L'ANSSI met ses guides à disposition sur la plateforme MesServicesCyber, dont La cybersécurité des systèmes industriels - Méthode de classification, publiée le 11 avril 2025. Le CLUSIF publie de son côté un dossier technique intitulé Guide de la cybersécurité des systèmes industriels, en version 2025, qui compte 107 pages et distingue trois niveaux de lecture, du tous publics à l'expert. Ces documents fixent la méthode ; ils ne dispensent pas de l'accès aux normes IEC 62443, qui restent payantes.

</details>

<details>
<summary>Qu'est-ce que le ReCyF et depuis quand est-il disponible ?</summary>

Le ReCyF, ou Référentiel Cyber France, liste les mesures recommandées par l'ANSSI pour atteindre les objectifs de sécurité fixés par la directive NIS 2. Il est mis à disposition depuis le 17 mars 2026, à ce stade en tant que document de travail, et correspond au référentiel de cybersécurité mentionné à l'article 14 du projet de loi Résilience. Non obligatoire par défaut, il permet aux futures entités assujetties qui décident de l'appliquer de s'en prévaloir en cas de contrôle de l'ANSSI. Un outil de comparaison de référentiels l'accompagne.

</details>

<details>
<summary>Comment suivre les vulnérabilités des équipements industriels ?</summary>

Le suivi repose sur trois flux complémentaires. Le NVD publie et note les CVE, y compris celles qui touchent les automates et les systèmes de conduite. Le CERT-FR diffuse les avis et alertes applicables au contexte français. La CISA maintient un flux d'avis spécifiquement consacré aux systèmes de contrôle industriel. MITRE ATT&CK for ICS complète l'ensemble par une cartographie des modes opératoires, qui comptait 12 tactiques et 90 techniques au 31 août 2026. Le préalable à tout suivi reste un inventaire à jour des équipements et de leurs versions, sans lequel un flux de vulnérabilités reste illisible.

</details>
