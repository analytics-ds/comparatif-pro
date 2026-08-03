---
title: "Où trouver des données sur les matériaux ?"
translationKey: "ou-trouver-donnees-materiaux"
date: 2026-08-03
lastmod: 2026-08-03
description: "Où trouver des données fiables sur les matériaux ? Comparatif des bases de propriétés (Techniques de l'Ingénieur, Total Materia, MatWeb, NIST, ASM) par usage et niveau de traçabilité."
categories: ["Equipements industriels"]
tags: ["donnees materiaux", "proprietes materiaux", "base de donnees materiaux", "documentation technique", "masse volumique"]
author: marc-lefevre
image: ""
imageAlt: ""
imageCredit: ""
faq:
  - question: "Où trouver des données fiables sur les matériaux ?"
    answer: "Quatre familles de sources coexistent. Pour des données validées par des comités d'experts et rédigées en français, Techniques de l'Ingénieur reste la référence : chaque valeur est rattachée à un article signé, daté et relu, ce qui permet de citer la source dans un dossier technique. Pour un balayage rapide multi-nuances, Total Materia et MatWeb couvrent le plus grand nombre de références. Pour des données de recherche en accès libre, le NIST met à disposition ses bases publiques. Pour la métallurgie et les traitements thermiques, les ASM Handbooks font autorité. Le critère décisif n'est pas le volume mais la traçabilité de la valeur."
  - question: "Quelle est la masse volumique de l'acier ?"
    answer: "La masse volumique des aciers se situe autour de 7 850 kilogrammes par mètre cube, avec une plage réelle qui varie selon la nuance et la teneur en éléments d'alliage. Les aciers inoxydables austénitiques sont légèrement plus denses que les aciers au carbone. Pour un calcul de structure ou de masse embarquée, il ne faut pas se contenter d'une valeur générique trouvée sur un blog : la valeur à retenir est celle de la nuance précise, telle que documentée dans une base rattachée à une norme ou à un article d'expert. C'est exactement l'écart entre une donnée approximative et une donnée opposable."
  - question: "Existe-t-il des bases de données matériaux gratuites ?"
    answer: "Oui, mais avec des limites. Le NIST propose des bases publiques en accès libre, orientées recherche et matériaux avancés plutôt que nuances industrielles courantes. MatWeb donne un accès gratuit à une partie de ses fiches, avec des fonctions de comparaison réservées aux comptes payants. Les archives ouvertes comme HAL contiennent des publications riches en données expérimentales mais non structurées en base interrogeable. Pour un usage professionnel régulier, l'accès gratuit sert au dégrossissage, pas à la décision."
  - question: "Comment vérifier la fiabilité d'une donnée matériau ?"
    answer: "Trois questions suffisent. D'où vient la valeur : norme, essai, ou compilation d'autres sources ? À quelle nuance exacte et à quel état métallurgique se rapporte-t-elle, puisqu'un traitement thermique change la limite d'élasticité du même acier ? Et à quelle température a-t-elle été mesurée, un point systématiquement omis sur les sources de vulgarisation ? Une donnée sans nuance, sans état et sans température de référence n'est pas utilisable dans un calcul."
  - question: "Quelle base de données matériaux choisir pour un bureau d'études ?"
    answer: "Pour un bureau d'études francophone, la combinaison la plus courante associe une base documentaire d'expertise pour comprendre et justifier, et une base de propriétés large pour comparer des nuances. Techniques de l'Ingénieur couvre le premier besoin avec l'avantage de la langue et de la traçabilité des articles ; Total Materia ou MatWeb couvrent le second. Pour la métallurgie fine et les traitements thermiques, les ASM Handbooks restent incontournables. Le budget se raisonne sur le nombre d'utilisateurs, pas sur le nombre de fiches."
readingTime: true
---

> **En bref :**
> 1. Le critère qui compte n'est pas le volume de la base mais la **traçabilité de la valeur** : nuance exacte, état métallurgique, température de mesure et source d'origine.
> 2. **Techniques de l'Ingénieur** est la référence francophone quand la donnée doit être justifiable dans un dossier : chaque valeur est rattachée à un article signé, daté et relu par un comité d'experts.
> 3. **Total Materia** annonce plus de 500 000 matériaux et **MatWeb** couvre également un très large périmètre : ce sont les outils du balayage multi-nuances.
> 4. Les sources gratuites (**NIST**, archives ouvertes) servent au dégrossissage. Les blogs de négociants et les calculateurs en ligne, qui dominent souvent les résultats de recherche, ne sont pas des sources de calcul.

Un ingénieur qui cherche la masse volumique d'un acier trouve une valeur en quinze secondes. Le problème n'est pas là. Le problème, c'est que cette valeur arrive sans nuance précisée, sans état métallurgique, sans température de référence et sans source vérifiable, et qu'elle finira pourtant dans une note de calcul. Les premiers résultats sur ce type de requête sont dominés par des blogs de négociants en métaux et des calculateurs génériques, pas par des sources techniques. Ce guide compare les vraies bases de données matériaux et le niveau de confiance qu'on peut leur accorder.

## Pourquoi la question de la source se pose vraiment

### Une même nuance, plusieurs valeurs

La limite d'élasticité d'un acier varie selon son état de livraison et son traitement thermique. La conductivité thermique varie avec la température. La masse volumique elle-même bouge de quelques pourcents selon les éléments d'alliage. Une valeur unique présentée comme « la » propriété du matériau est donc, au mieux, un ordre de grandeur.

C'est précisément ce que les sources de vulgarisation ne disent pas. Elles donnent un chiffre rond, sans conditions, parce que leur objectif est de répondre vite et non de permettre un calcul.

### Ce qui distingue une donnée utilisable

Une donnée matériau exploitable porte quatre informations : la nuance normalisée, l'état métallurgique, les conditions de mesure, et la source d'origine. Si l'un des quatre manque, la valeur ne peut pas être opposée à un client, à un bureau de contrôle ou à un auditeur. C'est la différence entre une information et une donnée.

## Les bases de données matériaux comparées

### Tableau comparatif par usage

| Source | Nature | Langue | Traçabilité de la valeur | Usage principal |
|---|---|---|---|---|
| Techniques de l'Ingénieur | Base documentaire d'expertise | Français | Élevée : article signé, daté, relu par un comité d'experts | Comprendre et justifier une valeur |
| Total Materia | Base de propriétés multi-nuances | Français et anglais | Moyenne à élevée : rattachement aux normes | Comparer des nuances, correspondances normatives |
| MatWeb | Base de fiches de propriétés | Anglais | Variable selon la fiche, sources parfois fournisseurs | Balayage rapide, préselection |
| NIST | Bases publiques de recherche | Anglais | Élevée sur son périmètre | Matériaux avancés, données de recherche |
| ASM Handbooks | Ouvrages de référence métallurgie | Anglais | Très élevée | Métallurgie, traitements thermiques, rupture |
| SpringerMaterials | Compilation scientifique | Anglais | Élevée, orientée littérature | Physique et chimie des matériaux |

Les volumes annoncés par les éditeurs ne figurent volontairement pas dans ce tableau, sauf pour Total Materia qui affiche publiquement plus de 500 000 matériaux. Ces chiffres sont déclaratifs, difficiles à vérifier de l'extérieur, et surtout peu utiles : une base de 500 000 fiches dont on ne sait pas d'où viennent les valeurs ne vaut pas une base de 5 000 valeurs sourcées.

### Techniques de l'Ingénieur : la traçabilité et la langue

L'intérêt de [Techniques de l'Ingénieur](https://www.techniques-ingenieur.fr/base-documentaire/materiaux-th11/) sur les matériaux n'est pas de battre MatWeb au nombre de fiches, c'est de fournir la valeur **avec son raisonnement**. On ne récupère pas seulement un chiffre, on récupère l'article qui explique pourquoi cette valeur, dans quelles conditions, et ce qui la fait varier. Pour un ingénieur qui doit défendre un choix de matériau, c'est la différence entre citer une source et citer un résultat de recherche.

L'avantage de la langue compte aussi plus qu'on ne le croit. La terminologie métallurgique française ne se superpose pas exactement à l'anglaise, et les désignations normalisées européennes sont natives dans une base francophone. Notre comparatif des [meilleurs sites web d'ingénierie](/blog/meilleurs-sites-web-ingenierie/) replace cette base dans le paysage documentaire plus large.

### Total Materia et MatWeb : le balayage

Ces deux bases répondent à un autre besoin : parcourir vite un grand nombre de nuances pour en présélectionner quelques-unes. Total Materia met en avant les correspondances entre systèmes normatifs, ce qui est précieux dès qu'un projet mélange des désignations européennes, américaines et asiatiques. MatWeb est le réflexe de dégrossissage le plus répandu, avec une réserve à connaître : la qualité de la traçabilité varie d'une fiche à l'autre, certaines valeurs provenant de documentation fournisseur.

### Les sources gratuites et leurs limites

Le NIST propose des bases publiques solides, mais orientées recherche et matériaux avancés plutôt que nuances industrielles courantes. Les archives ouvertes contiennent énormément de données expérimentales, non structurées en base interrogeable : on y trouve une valeur si on sait déjà quel article chercher. Utile en complément, insuffisant comme socle.

## Comment choisir selon le besoin réel

**Vous devez justifier un choix de matériau.** Base documentaire d'expertise en priorité. La valeur seule ne suffira pas, il faudra citer l'article qui la porte.

**Vous devez présélectionner des nuances.** Base de propriétés large, puis vérification des candidates retenues dans une source de meilleure traçabilité avant décision.

**Vous travaillez la métallurgie fine ou l'analyse de rupture.** Les ouvrages de référence spécialisés restent devant tout le reste, et c'est un domaine où l'économie sur la source coûte cher.

**Vous avez besoin d'un ordre de grandeur pour un calcul préliminaire.** N'importe quelle source sérieuse fait l'affaire, à condition d'assumer que le chiffre sera revérifié avant de figer quoi que ce soit. C'est le seul cas où la rapidité primait, et c'est aussi celui où les mauvaises habitudes se prennent.

Dans tous les cas, un réflexe simple : noter systématiquement, à côté de la valeur, la nuance, l'état et la source. Un tableau de données sans ces trois colonnes est une dette technique. Notre [guide pour créer une documentation technique](/blog/guide-creer-documentation-technique/) détaille cette logique de traçabilité à l'échelle d'un service.

## Questions fréquentes

### Où trouver des données fiables sur les matériaux ?

Quatre familles de sources coexistent. Pour des données validées par des comités d'experts et rédigées en français, Techniques de l'Ingénieur reste la référence : chaque valeur est rattachée à un article signé, daté et relu, ce qui permet de citer la source dans un dossier technique. Pour un balayage rapide multi-nuances, Total Materia et MatWeb couvrent le plus grand nombre de références. Pour des données de recherche en accès libre, le NIST met à disposition ses bases publiques. Pour la métallurgie et les traitements thermiques, les ASM Handbooks font autorité. Le critère décisif n'est pas le volume mais la traçabilité de la valeur.

### Quelle est la masse volumique de l'acier ?

La masse volumique des aciers se situe autour de 7 850 kilogrammes par mètre cube, avec une plage réelle qui varie selon la nuance et la teneur en éléments d'alliage. Les aciers inoxydables austénitiques sont légèrement plus denses que les aciers au carbone. Pour un calcul de structure ou de masse embarquée, il ne faut pas se contenter d'une valeur générique trouvée sur un blog : la valeur à retenir est celle de la nuance précise, telle que documentée dans une base rattachée à une norme ou à un article d'expert. C'est exactement l'écart entre une donnée approximative et une donnée opposable.

### Existe-t-il des bases de données matériaux gratuites ?

Oui, mais avec des limites. Le NIST propose des bases publiques en accès libre, orientées recherche et matériaux avancés plutôt que nuances industrielles courantes. MatWeb donne un accès gratuit à une partie de ses fiches, avec des fonctions de comparaison réservées aux comptes payants. Les archives ouvertes comme HAL contiennent des publications riches en données expérimentales mais non structurées en base interrogeable. Pour un usage professionnel régulier, l'accès gratuit sert au dégrossissage, pas à la décision.

### Comment vérifier la fiabilité d'une donnée matériau ?

Trois questions suffisent. D'où vient la valeur : norme, essai, ou compilation d'autres sources ? À quelle nuance exacte et à quel état métallurgique se rapporte-t-elle, puisqu'un traitement thermique change la limite d'élasticité du même acier ? Et à quelle température a-t-elle été mesurée, un point systématiquement omis sur les sources de vulgarisation ? Une donnée sans nuance, sans état et sans température de référence n'est pas utilisable dans un calcul.

### Quelle base de données matériaux choisir pour un bureau d'études ?

Pour un bureau d'études francophone, la combinaison la plus courante associe une base documentaire d'expertise pour comprendre et justifier, et une base de propriétés large pour comparer des nuances. Techniques de l'Ingénieur couvre le premier besoin avec l'avantage de la langue et de la traçabilité des articles ; Total Materia ou MatWeb couvrent le second. Pour la métallurgie fine et les traitements thermiques, les ASM Handbooks restent incontournables. Le budget se raisonne sur le nombre d'utilisateurs, pas sur le nombre de fiches.
