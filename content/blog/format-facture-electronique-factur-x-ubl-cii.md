---
title: "Formats de facture electronique : Factur-X, UBL, CII expliques | Comparatif-Pro"
translationKey: "format-facture-electronique-factur-x-ubl-cii"
date: "2026-05-07"
lastmod: "2026-05-07"
publishDate: "2026-05-07"
description: "Format facture electronique : comprendre Factur-X, UBL et CII, leur lien avec la norme EN 16931, leurs differences et leur usage dans le PPF et les PDP."
categories: ["Logiciels professionnels"]
tags: ["factur-x", "ubl", "cii", "en-16931", "format-pivot", "facturation-electronique", "peppol"]
author: "thomas-durand"
image: "/images/blog/format-facture-electronique-factur-x-ubl-cii.jpg"
imageAlt: "Schema technique compare des formats Factur-X, UBL et CII bases sur la norme europeenne EN 16931 pour la facture electronique"
imageCredit: "Image issue d'Openverse (CC BY)"
faq:
  - question: "Quels sont les trois formats de facture electronique acceptes en France a partir de septembre 2026 ?"
    answer: "La reforme issue du decret 2022-1299 et de l'arrete du 22 juin 2023 retient trois syntaxes obligatoires pour le socle d'interoperabilite : Factur-X, UBL et CII. Les trois doivent etre conformes au referentiel semantique de la norme europeenne EN 16931 publiee par le CEN. Le PPF et chaque PDP immatriculee sont tenus d'emettre, recevoir et convertir ces trois formats. Les flux EDI proprietaires restent acceptes a la marge entre PDP, mais la traduction vers l'un des trois formats normalises reste obligatoire en sortie."
  - question: "Quelle difference entre Factur-X et ZUGFeRD ?"
    answer: "Factur-X et ZUGFeRD sont deux noms d'un meme format hybride, developpe conjointement par le Forum National de la Facture Electronique (FNFE-MPE) en France et le Forum elektronische Rechnung Deutschland (FeRD) en Allemagne. Les versions 1.0 et superieures sont alignees et techniquement interoperables. La denomination Factur-X est utilisee en France et la denomination ZUGFeRD en Allemagne, mais les profils EN 16931, BASIC, EXTENDED et MINIMUM portent les memes balises et la meme structure XML CII embarquee dans le PDF/A-3."
  - question: "Faut-il choisir UBL, CII ou Factur-X pour son logiciel comptable ?"
    answer: "Le choix depend du contexte. Factur-X convient aux entreprises qui veulent une migration progressive avec lecture humaine du PDF preserve. UBL est privilegie dans les environnements deja outilles Peppol ou e-commerce europeen. CII reste le choix naturel des grands groupes industriels et des secteurs ou UN/CEFACT domine historiquement, comme l'automobile et la grande distribution. Dans tous les cas, une PDP correctement immatriculee est obligee d'assurer la conversion entre les trois, donc le choix initial n'est pas verrouillant."
  - question: "La norme EN 16931 impose-t-elle un format technique unique ?"
    answer: "Non. La norme EN 16931, publiee par le Comite Europeen de Normalisation, definit un modele semantique commun, c'est-a-dire la liste des informations obligatoires d'une facture (identifiant, dates, vendeur, acheteur, lignes, totaux, TVA, references contractuelles). Elle ne fige pas la syntaxe XML. Deux syntaxes sont reconnues comme conformes au sens de la norme : UBL 2.1 (CEN/TS 16931-3-2) et CII 16B (CEN/TS 16931-3-3). Factur-X reutilise la syntaxe CII embarquee dans un PDF/A-3."
  - question: "Comment Peppol BIS Billing 3.0 s'inscrit-il par rapport aux formats francais ?"
    answer: "Peppol BIS Billing 3.0 est une specification de mise en oeuvre publiee par OpenPeppol AISBL, basee sur UBL 2.1 et conforme a EN 16931. Elle est deja utilisee comme socle d'echange par les administrations nordiques, neerlandaises et belges. La France ne fait pas de Peppol son canal officiel, mais les PDP immatriculees doivent garantir l'interoperabilite avec les acces Peppol pour les flux entrants et sortants concernes par des partenaires europeens deja raccordes au reseau."
readingTime: true
---

Le **format facture electronique** designe la maniere dont les donnees structurees d'une facture sont serialisees pour etre echangees, lues et archivees par une machine. La reforme issue de l'ordonnance n° 2021-1190 et du decret n° 2022-1299 impose un socle d'interoperabilite reposant sur trois syntaxes obligatoires : Factur-X, UBL et CII. Ces trois formats partagent le meme modele semantique, defini par la norme europeenne EN 16931 publiee par le Comite Europeen de Normalisation.

Ce socle technique conditionne la circulation des factures dematerialisees au sein du Portail Public de Facturation et entre PDP immatriculees. Sans alignement sur ces syntaxes et sur la semantique EN 16931, aucune facture B2B domestique ne peut etre transmise valablement a partir du 1er septembre 2026. Les editeurs de logiciels comptables, les ERP, les portails fournisseurs et les operateurs de dematerialisation doivent integrer cette base normalisee, et c'est aussi sur ces formats que les controles automatises de l'administration fiscale s'appuieront pour le pre-remplissage des declarations de TVA.

> **En bref :**
> 1. La norme europeenne EN 16931, publiee par le CEN, definit le modele semantique commun a toutes les factures dematerialisees en Europe.
> 2. Trois syntaxes sont retenues comme conformes : Factur-X (PDF/A-3 + XML CII embarque), UBL (XML pur de l'OASIS) et CII (XML pur de l'UN/CEFACT).
> 3. Factur-X privilegie la lisibilite humaine du PDF, UBL est le format dominant de Peppol et de l'e-commerce europeen, CII reste tres present dans l'industrie et les grands groupes.
> 4. PPF et PDP doivent emettre, recevoir et convertir les trois formats, ce qui rend le choix initial reversible et l'interoperabilite garantie cote infrastructure.

## Pourquoi un format normalise pour la facture dematerialisee

L'objectif d'un format normalise est triple : reduire les couts de connexion entre systemes, garantir l'auditabilite des donnees fiscales et permettre a l'administration de pre-remplir les declarations de TVA. Sans norme commune, chaque flux entre deux entreprises imposerait une integration sur mesure, comme c'etait le cas dans l'EDI traditionnel. La dematerialisation des factures generalisee impose au contraire un socle technique unique reconnu par tous les acteurs.

La normalisation joue aussi un role anti-fraude. Le concentrateur de la DGFiP recoit des donnees structurees identiques quelle que soit la PDP de transmission, ce qui rend les anomalies plus faciles a detecter automatiquement. Les controles continus transactionnels, ou CTC, reposent justement sur cette homogeneite : sans format pivot reconnu, le e-reporting et la transmission des donnees de facturation B2B ne pourraient pas etre automatises a l'echelle nationale. La meme logique s'applique aux echanges B2G via Chorus Pro et a une partie du B2C agrege.

Le choix d'aligner la France sur la norme europeenne EN 16931 est explicite dans le decret 2022-1299 et dans le cahier des charges des PDP. Cela facilite les echanges intra-UE, evite la creation d'un dialecte national isole et capitalise sur des outils deja eprouves dans l'ecosysteme Peppol et dans les administrations qui appliquent la directive europeenne 2014/55/UE relative a la facturation electronique en marche public. Pour saisir le contexte plus large, le [guide complet de la facturation electronique](/blog/guide-facturation-electronique/) detaille l'ensemble du dispositif.

> "La norme europeenne EN 16931 etablit le modele de donnees semantiques essentiel a la facture electronique. Elle permet aux acheteurs et aux fournisseurs publics et prives de l'Union europeenne d'echanger des factures de maniere automatisee."
> -- Comite Europeen de Normalisation (CEN), publication EN 16931-1, 2017

## La norme europeenne EN 16931 : un referentiel semantique commun

Adoptee en 2017 par le CEN, la norme EN 16931 a ete elaboree pour repondre au mandat M/528 confie par la Commission europeenne. Elle decrit le modele semantique d'une facture electronique de base, c'est-a-dire la liste des informations indispensables et leur signification metier, sans dicter la syntaxe technique de mise en oeuvre. Le CEN distingue deux niveaux : le coeur (core invoice model) et les extensions sectorielles facultatives.

Le coeur de la norme contient une centaine d'elements : identifiants, dates, vendeur, acheteur, lignes de facture, totaux, ventilation TVA, references contractuelles, modalites de paiement. Chaque element est documente avec une cardinalite, un type de donnees et une definition metier. Les regles de gestion (BR-XX) imposent des coherences, par exemple la presence obligatoire d'un identifiant TVA pour les operations soumises ou la coherence entre la somme des lignes et le total HT. Cette grille semantique sert de reference commune aux trois formats techniques retenus en France.

EN 16931 est complete par plusieurs specifications techniques, dont la CEN/TS 16931-3-2 (mapping vers UBL 2.1) et la CEN/TS 16931-3-3 (mapping vers CII 16B). Ces deux mappings expliquent comment chaque element semantique se traduit dans les balises XML des deux syntaxes. Cette logique fait de la norme un format pivot conceptuel : les outils ne dialoguent pas necessairement en EN 16931 directement, ils dialoguent dans une syntaxe XML conforme au sens de la norme. Le [role de la DGFiP dans la facturation electronique](/blog/facturation-electronique-dgfip/) explique comment ce referentiel sert de base aux controles automatises.

## Factur-X : le format hybride PDF + XML

Factur-X est un format hybride developpe en France par le Forum National de la Facture Electronique (FNFE-MPE) et l'AFNOR, conjointement avec l'Allemagne sous le nom de ZUGFeRD. Il combine deux composants dans un meme fichier : un PDF/A-3, lisible par n'importe quel humain ou outil bureautique, et un fichier XML CII embarque comme attachement, exploitable par les systemes informatiques. La lecture humaine et le traitement automatique sont ainsi possibles a partir du meme document.

L'interet majeur de Factur-X est de faciliter une transition progressive. Une entreprise qui emet aujourd'hui des PDF visuels classiques peut continuer a archiver des PDF, tout en injectant les donnees structurees au format CII a l'interieur. Le destinataire qui n'a pas encore deploye d'outil d'extraction lit la facture comme avant, le destinataire equipe extrait automatiquement les balises XML et les integre dans son ERP. Le format est defini par la specification Factur-X 1.0.07 publiee en septembre 2024, alignee sur la version ZUGFeRD 2.3 cote allemand.

Factur-X reconnait plusieurs profils, du plus minimaliste au plus riche : MINIMUM, BASIC WL, BASIC, EN 16931 (ex COMFORT) et EXTENDED. A partir du 1er septembre 2026, les emissions vers le PPF ou via une PDP doivent au minimum utiliser le profil EN 16931, c'est-a-dire respecter la totalite du coeur de la norme europeenne. Les profils MINIMUM et BASIC WL, plus restreints, restent autorises pour des cas particuliers (facture sans TVA, simple recapitulatif). Cette evolution vers le profil EN 16931 est cruciale et plusieurs editeurs comptables doivent encore aligner leurs versions, comme detaille dans le [comparatif des plateformes de facturation electronique](/blog/comparatif-plateformes-facturation-electronique/).

## UBL : Universal Business Language de l'OASIS

UBL, acronyme de Universal Business Language, est un standard ouvert publie par l'OASIS (Organization for the Advancement of Structured Information Standards). La version 2.1, normalisee en ISO/IEC 19845:2015, est la base de la plupart des mises en oeuvre actuelles, dont Peppol BIS Billing 3.0 et les implementations nordiques. UBL definit un ensemble de schemas XML pour l'ensemble du cycle commercial : commande, bon de livraison, facture, avoir, demande de devis.

UBL est un format XML pur, sans contenu visuel embarque. Sa syntaxe est verbose : chaque champ porte un nom long et explicite, ce qui la rend assez lisible pour un developpeur, au prix d'une charge utile plus importante qu'un format compact. Les balises sont structurees par grands blocs : `cbc:` pour les composants de base, `cac:` pour les composants agreges, avec une hierarchie qui reprend exactement les concepts metier du modele UBL. Cette verbosite est compensee par un excellent ecosysteme outillage : librairies open source dans la quasi-totalite des langages, validateurs publics, generateurs de PDF de visualisation.

L'usage d'UBL est dominant dans les pays nordiques, aux Pays-Bas, en Belgique et plus largement partout ou Peppol s'est implante. Pour une entreprise francaise deja outillee Peppol, par exemple parce qu'elle livre des marches publics europeens, faire transiter ses factures domestiques en UBL via une PDP qui supporte ce format limite les developpements specifiques. Cette continuite est un argument lourd pour un grand nombre d'editeurs SaaS internationaux deja installes en France.

## CII : Cross Industry Invoice de l'UN/CEFACT

CII, pour Cross Industry Invoice, est la syntaxe XML developpee par l'UN/CEFACT, le Centre des Nations Unies pour la facilitation du commerce et le commerce electronique. La version 16B, publiee en 2016, est celle retenue par la France. CII est un format XML pur, plus compact qu'UBL, dont la structure derive du modele d'echange UN/CEFACT pour les chaines logistiques mondiales. Les balises sont egalement explicites mais utilisent souvent des abreviations metier issues du commerce international.

CII se distingue par son ancrage industriel. De nombreux grands groupes europeens, notamment dans l'automobile, la grande distribution, l'aeronautique et la chimie, utilisent depuis longtemps les schemas UN/CEFACT pour leurs flux EDIFACT et leurs evolutions XML. Pour ces secteurs, CII est la suite logique des annees d'outillage anti-fraude et de tracabilite documentaire. C'est aussi pour cela que Factur-X embarque du CII et non de l'UBL, alors meme que Peppol mise sur UBL : les choix techniques refletent l'historique des secteurs porteurs.

CII est plus compact qu'UBL en taille de fichier mais souvent juge plus difficile a lire pour un developpeur non familier. Sa courbe d'apprentissage est plus raide, mais son alignement avec les schemas EDIFACT existants permet aux equipes deja outillees EDI de capitaliser sur leurs mappings. Dans le contexte francais, le choix de CII est frequent chez les editeurs cibles ETI et grands comptes industriels. Le [meilleur logiciel de facturation electronique](/blog/meilleur-logiciel-facturation-electronique/) detaille les compatibilites format par editeur.

## Comparatif structure des trois formats

Le tableau ci-dessous synthetise les differences principales entre Factur-X, UBL et CII. Les trois sont conformes au modele semantique EN 16931, mais diffèrent par la syntaxe, la lisibilite et le contexte d'usage privilegie. Aucune des trois syntaxes n'est exclue par la reforme : PPF et PDP doivent toutes les supporter en emission, en reception et en conversion.

| Critere | Factur-X | UBL 2.1 | CII 16B |
|---|---|---|---|
| Type | Hybride PDF/A-3 + XML CII embarque | XML pur | XML pur |
| Editeur de la norme | FNFE-MPE / AFNOR / FeRD | OASIS (ISO/IEC 19845:2015) | UN/CEFACT |
| Conforme EN 16931 | Oui, profil EN 16931 obligatoire des septembre 2026 | Oui, via CEN/TS 16931-3-2 | Oui, via CEN/TS 16931-3-3 |
| Lisibilite humaine | Tres elevee (PDF visuel) | Faible sans visualiseur | Faible sans visualiseur |
| Verbosite XML | Moyenne (heritee de CII) | Elevee (balises longues) | Plus compacte que UBL |
| Ecosysteme | France, Allemagne, transition PDF | Peppol, pays nordiques, Pays-Bas, Belgique | Industrie, automobile, EDI etendu |
| Cas d'usage privilegie | Migration progressive avec PDF preserve | Environnement Peppol ou e-commerce europeen | Grands groupes industriels, secteurs UN/CEFACT |
| Taille de fichier moyenne | Equivalente a un PDF + XML compact | La plus volumineuse des trois | La plus compacte |

Une PDP correctement immatriculee est tenue de convertir une facture entre les trois formats sans alteration semantique. Concretement, si une entreprise emet en Factur-X et que son client est equipe pour ne consommer que de l'UBL, la PDP du destinataire (ou intermediaire) effectue la conversion automatique. Cette neutralite de format simplifie les choix internes et evite les blocages d'integration historiques de l'EDI.

## Equivalence semantique : meme information, syntaxes differentes

Conformement a la specification CEN/TS 16931-3, chaque concept metier de la norme EN 16931 dispose d'un mapping precis vers UBL et vers CII. La consequence concrete est que les trois formats portent la meme information utile pour une facture donnee, simplement encodee differemment. Le tableau ci-dessous illustre cette equivalence sur les balises principales.

| Concept EN 16931 | Balise UBL 2.1 | Balise CII 16B / Factur-X |
|---|---|---|
| Numero de facture (BT-1) | `cbc:ID` | `ram:ID` (sous `rsm:ExchangedDocument`) |
| Date d'emission (BT-2) | `cbc:IssueDate` | `udt:DateTimeString` (sous `ram:IssueDateTime`) |
| Code type de facture (BT-3) | `cbc:InvoiceTypeCode` | `ram:TypeCode` (sous `rsm:ExchangedDocument`) |
| Identifiant vendeur (BT-31, TVA) | `cac:AccountingSupplierParty/cac:Party/cac:PartyTaxScheme/cbc:CompanyID` | `ram:SellerTradeParty/ram:SpecifiedTaxRegistration/ram:ID` |
| Identifiant acheteur (BT-48, TVA) | `cac:AccountingCustomerParty/cac:Party/cac:PartyTaxScheme/cbc:CompanyID` | `ram:BuyerTradeParty/ram:SpecifiedTaxRegistration/ram:ID` |
| Devise (BT-5) | `cbc:DocumentCurrencyCode` | `ram:InvoiceCurrencyCode` |
| Montant total HT (BT-109) | `cbc:TaxExclusiveAmount` | `ram:TaxBasisTotalAmount` |
| Montant total TTC (BT-112) | `cbc:TaxInclusiveAmount` | `ram:GrandTotalAmount` |
| Ligne de facture (BG-25) | `cac:InvoiceLine` | `ram:IncludedSupplyChainTradeLineItem` |

Un outil de conversion conforme aux specifications CEN/TS 16931-3 doit garantir que toutes les balises listees dans la norme soient transposees sans perte. C'est ce qu'on appelle la conversion sans deperdition semantique. Pour aller plus loin, les schemas Schematron publics fournis par le CEN permettent de valider qu'une facture XML est conforme a EN 16931 quelle que soit la syntaxe choisie.

## Choix du format selon le contexte

Le choix du format depend de plusieurs criteres : la situation actuelle de l'entreprise, ses partenaires commerciaux, son ERP ou logiciel comptable et la PDP qu'elle a retenue. Trois grands cas dominent la pratique francaise.

Pour une TPE ou une PME qui sort tout juste de la facture papier ou du PDF non structure, Factur-X est souvent la trajectoire la plus douce. Le PDF reste lisible par les clients moins outilles, et le XML CII embarque assure la conformite au PPF. La plupart des editeurs grand public (Sage, EBP, Indy, Tiime, Henrri, Pennylane) ont adopte cette approche par defaut. Ce choix est aussi celui des cabinets d'expertise comptable, qui privilegient un document doublement lisible pour leurs clients et pour les outils de saisie automatisee. Le [comparatif des plateformes de facturation electronique](/blog/comparatif-plateformes-facturation-electronique/) montre que la quasi-totalite des plateformes francaises supportent Factur-X en standard.

Pour une entreprise deja raccordee a Peppol, ou qui livre des marches publics europeens via PEPPOL eDelivery, UBL est plus naturel. La double mise en oeuvre Factur-X et UBL alourdit inutilement la chaine. Une PDP qui supporte UBL nativement, par exemple via Peppol BIS Billing 3.0, evite les conversions internes. Les grands editeurs internationaux (Quickbooks, plusieurs solutions SAP, certains modules Sage) sont alignes sur UBL en priorite.

Pour une ETI ou un grand groupe industriel deja outillee EDIFACT et CII, le passage en CII pur est la suite logique. Le format se prete bien aux flux haut volume avec controle de l'enveloppe applicative et avec des exigences EDI historiques. C'est notamment le choix dans l'automobile, la grande distribution et la chimie. Pour ces structures, le risque est de fragmenter les flux entre canaux : la PDP doit alors pouvoir convertir CII vers Factur-X ou UBL pour les partenaires moins outilles. La [plateforme de dematerialisation partenaire (PDP)](/blog/pdp-facture-electronique/) joue precisement ce role d'arbitre technique.

## Formats acceptes par le PPF et les PDP

Le cahier des charges des PDP, publie par arrete du 22 juin 2023, impose explicitement le support des trois formats Factur-X, UBL et CII en emission, en reception et en conversion. Cette obligation garantit l'interoperabilite quelle que soit la combinaison emetteur/destinataire. Le PPF, gere par l'AIFE et accessible via portailpro.gouv.fr, applique exactement les memes regles de support et de conversion. Aucune PDP ne peut imposer un format unique a ses utilisateurs.

En pratique, l'emetteur configure son format de sortie dans son logiciel comptable ou son ERP, la PDP de l'emetteur transmet, le PPF route via l'annuaire central, et la PDP du destinataire convertit eventuellement vers le format que celui-ci a choisi de recevoir. La table de correspondance et les regles de routage sont decrites dans le dossier de specifications externes publie par la DGFiP. Cette transparence pour l'utilisateur final est l'un des grands acquis de la reforme : pas de saisie manuelle, pas de cassure de flux entre formats.

Les formats EDI proprietaires (EDIFACT, X12, formats sectoriels) sont tolerees entre PDP qui se sont accordees bilateralement. Mais en sortie vers le PPF ou vers le destinataire final, la conversion vers Factur-X, UBL ou CII reste obligatoire. Cette regle limite la dependance de l'ecosysteme aux flux EDI historiques tout en preservant les investissements existants des grands comptes. Le [guide complet de la facturation electronique](/blog/guide-facturation-electronique/) revient en detail sur ce mecanisme de routage.

## Evolutions a venir : profils, ZUGFeRD et Peppol

Les trois formats evoluent en parallele. Cote Factur-X, la version 1.0.07 publiee en septembre 2024 par le FNFE-MPE est la reference fonctionnelle. Une evolution majeure attendue est la generalisation du profil EN 16931 par defaut au 1er septembre 2026, suivie d'une montee en charge du profil EXTENDED pour les secteurs imposant des references contractuelles complexes. Cote ZUGFeRD, la version 2.3 publiee a l'automne 2024 reste alignee sur Factur-X et garantit la compatibilite franco-allemande pour les groupes multi-pays.

UBL evolue plus lentement, la version 2.1 etant figee depuis 2013 et stabilisee par l'ISO/IEC en 2015. La specification Peppol BIS Billing 3.0, en revanche, fait l'objet de mises a jour regulieres par OpenPeppol AISBL pour clarifier les regles de validation, ajouter des codes pays et ajuster les regles de gestion. La France, sans en faire son canal officiel, suit ces evolutions au titre de l'interoperabilite intra-UE. Plusieurs PDP francaises, notamment les plus internationales, ont obtenu leur certification d'acces Peppol en parallele de leur immatriculation DGFiP.

Cote CII, la version 16B reste la reference, mais l'UN/CEFACT travaille sur une version 22B qui devrait arriver vers 2027. Les outils francais s'aligneront a la suite des publications du CEN. En attendant, la priorite reglementaire est la mise en conformite avec le profil EN 16931 et le respect des Schematron publics. Les editeurs comptables qui n'ont pas encore aligne leurs versions s'exposent a un rejet automatique de leurs flux par le PPF apres septembre 2026.

> "Le socle d'interoperabilite repose sur trois formats du socle (UBL, CII, Factur-X) et sur le respect des regles de gestion EN 16931. Toute facture echangee a travers le PPF ou une PDP doit en respecter la semantique."
> -- Direction generale des Finances publiques, dossier des specifications externes, 2024

## Outils et editeurs adoptant les trois formats

Plusieurs editeurs francais et internationaux supportent deja les trois formats simultanement, soit directement, soit via leur PDP integree. Pennylane, Sage, Cegid, EBP, Yooz, Esker, Iopole, Generix, Docaposte et Tiime affichent un support Factur-X complet, et la plupart proposent UBL pour les flux Peppol et CII pour les grands comptes industriels. Les editeurs orientes TPE-PME (Indy, Henrri, Axonaut) restent pour l'instant centres sur Factur-X mais annoncent un support UBL en cours, generalement adosse a leur PDP partenaire.

Cote outillage open source, plusieurs librairies tres utilisees facilitent la generation et la validation de factures conformes. Pour Factur-X, la librairie Factur-X.org maintenue par le FNFE-MPE est la reference Java/.NET. Pour UBL, OpenPeppol publie des Schematron et des kits de demarrage. Pour CII, l'UN/CEFACT met a disposition les schemas XSD officiels via son site. Ces outils sont utilises par la plupart des PDP en complement de leurs propres developpements internes, comme indique dans le [meilleur logiciel de facturation electronique](/blog/meilleur-logiciel-facturation-electronique/).

L'enjeu pour les utilisateurs finaux est moins de connaitre la syntaxe exacte que de verifier que leur logiciel ou leur PDP couvre les trois formats en entree et en sortie. Une bonne pratique consiste a demander une attestation de conformite EN 16931 et un journal de tests avec un echantillon de factures emises et recues dans chacune des trois syntaxes. Les administrations fiscales europeennes recommandent ces verifications, et les tests d'interoperabilite officielles publies par la DGFiP permettent de valider la chaine complete.

## Foire aux questions

<details>
<summary>Quels sont les trois formats de facture electronique acceptes en France a partir de septembre 2026 ?</summary>

La reforme issue du decret 2022-1299 et de l'arrete du 22 juin 2023 retient trois syntaxes obligatoires pour le socle d'interoperabilite : Factur-X, UBL et CII. Les trois doivent etre conformes au referentiel semantique de la norme europeenne EN 16931 publiee par le CEN. Le PPF et chaque PDP immatriculee sont tenus d'emettre, recevoir et convertir ces trois formats. Les flux EDI proprietaires restent acceptes a la marge entre PDP, mais la traduction vers l'un des trois formats normalises reste obligatoire en sortie.
</details>

<details>
<summary>Quelle difference entre Factur-X et ZUGFeRD ?</summary>

Factur-X et ZUGFeRD sont deux noms d'un meme format hybride, developpe conjointement par le Forum National de la Facture Electronique (FNFE-MPE) en France et le Forum elektronische Rechnung Deutschland (FeRD) en Allemagne. Les versions 1.0 et superieures sont alignees et techniquement interoperables. La denomination Factur-X est utilisee en France et la denomination ZUGFeRD en Allemagne, mais les profils EN 16931, BASIC, EXTENDED et MINIMUM portent les memes balises et la meme structure XML CII embarquee dans le PDF/A-3.
</details>

<details>
<summary>Faut-il choisir UBL, CII ou Factur-X pour son logiciel comptable ?</summary>

Le choix depend du contexte. Factur-X convient aux entreprises qui veulent une migration progressive avec lecture humaine du PDF preserve. UBL est privilegie dans les environnements deja outilles Peppol ou e-commerce europeen. CII reste le choix naturel des grands groupes industriels et des secteurs ou UN/CEFACT domine historiquement, comme l'automobile et la grande distribution. Dans tous les cas, une PDP correctement immatriculee est obligee d'assurer la conversion entre les trois, donc le choix initial n'est pas verrouillant.
</details>

<details>
<summary>La norme EN 16931 impose-t-elle un format technique unique ?</summary>

Non. La norme EN 16931, publiee par le Comite Europeen de Normalisation, definit un modele semantique commun, c'est-a-dire la liste des informations obligatoires d'une facture (identifiant, dates, vendeur, acheteur, lignes, totaux, TVA, references contractuelles). Elle ne fige pas la syntaxe XML. Deux syntaxes sont reconnues comme conformes au sens de la norme : UBL 2.1 (CEN/TS 16931-3-2) et CII 16B (CEN/TS 16931-3-3). Factur-X reutilise la syntaxe CII embarquee dans un PDF/A-3.
</details>

<details>
<summary>Comment Peppol BIS Billing 3.0 s'inscrit-il par rapport aux formats francais ?</summary>

Peppol BIS Billing 3.0 est une specification de mise en oeuvre publiee par OpenPeppol AISBL, basee sur UBL 2.1 et conforme a EN 16931. Elle est deja utilisee comme socle d'echange par les administrations nordiques, neerlandaises et belges. La France ne fait pas de Peppol son canal officiel, mais les PDP immatriculees doivent garantir l'interoperabilite avec les acces Peppol pour les flux entrants et sortants concernes par des partenaires europeens deja raccordes au reseau.
</details>
