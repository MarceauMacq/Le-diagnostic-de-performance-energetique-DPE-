Par Maxence Briquet, Matthieu Delafon, Abdelkarim Khalid, Marceau Macquignon, Marie Poff.

Voici les résultats de notre étude sur la bse de données "DPE logements existants depuis juillet 2021", disponible à l'adresse suivante : https://data.ademe.fr/datasets/dpe-v2-logements-existants

## Introduction

Matthieu Delafon - to be uploaded soon

## I. La construction d'un indicateur pour quantifier la performance énergétique

## II. Les limites de cet indicateur

## III. Les usages de cet indicateur

## IV. Les usages que permettent cette base de données

### La collecte des données par l'ADEME
Depuis 2013, et faisant suite à la Loi n° 2010-788 du 12 juillet 2010 portant engagement national pour l'environnement, tous les DPE réalisés doivent être transmis à l’ADEME. Ces dispositions ont été renforcées par l’Arrêté du 31 mars 2021 relatif aux méthodes et procédures applicables au diagnostic de performance énergétique et aux logiciels l’établissant, précisant que la transmission des diagnostics réalisés par les logiciels conformes à la méthode de calcul dite “3CL” est obligatoire, et se fait par voie informatique.

L’ADEME a ainsi créé l’Observatoire DPE pour collecter et publier ces données, et notamment permettre de retrouver le contenu d’un DPE, d’avoir accès à une liste de diagnostiqueurs, de pouvoir consulter des statistiques ou télécharger des base de données, et potentiellement à l’avenir d’effectuer des simulations de DPE. 

Depuis la généralisation de cette nouvelle méthode de calcul, au 1er juillet 2021, plus de 3 millions de DPE logements ont été reçus par l’Observatoire DPE de l’ADEME, 268 297 pour le mois d’octobre 2022.

Depuis le 3 août 2022, les DPE collectés depuis le 1er juillet 2021 par l’Observatoire DPE sont disponibles en Open Data, sur le site de l’observatoire DPE ou sur le site de l’ADEME. 

### Manipulations de la base de données pour obtenir un échantillon plus représentatif du parc de logements français
L’une des limites principales de l’exploitation de cette base de données elle sa non-représentativité de l’ensemble du parc de logement en France. L’INSEE dénombrait 37,6 millions de logements en France hors Mayotte au 1er janvier 2022, presque 8,5% des logements français figurent donc dans la bse de données des DPE logements réalisé depuis le 1er juillet 2021 (en admettant qu’il y ai peu de doublons, ce qui est une autre limite de la base de données). Malgré cette taille importante, le DPE ne concerne que les logements neufs, en vente ou en location. Le parc locatif et de logements neufs y est donc surreprésenté. 

Il est cependant possible de redresser cette base de données (en pondérant donc chaque DPE selon les caractéristiques du logement, pour obtenir un échantillon plus représentatif. Pour se faire, plusieurs travaux utilisent les données des Fichiers démographiques sur les logements et les individus (Fidéli) de l’INSEE, qui intègre des données fiscales pour caractériser les différents logements.

On peut citer une étude menée par l’Observatoire national de la rénovation énergétique (ONRE, “Le parc de logements par classe de performance énergétique au 1er janvier 2022”, juillet 2022), qui utilise cette méthode de redressement, et détaille en annexe cette méthodologie. Il faut ainsi noter que l’étape d'appariement entre la bse de données des DPE et le répertoire Fidéli n’est pas toujours exact, car les logements ne disposent pas d’un identifiant propre. C’est donc selon leurs caractéristiques (taille, date de construction, type de logement, localisation géographique, etc.) que l’association est faite entre un DPE et les informations fiscales du répertoire Fidéli.

![Sans titre](https://user-images.githubusercontent.com/115630234/203338449-3763126e-3587-41c8-88a9-467bedb5bc88.png)
Source : Fidéli 2020 ; base des DPE décembre 2021-mars 2022 de l’Ademe, calculs SDSE, à partir de ONRE, “Le parc de logements par classe de performance énergétique au 1er janvier 2022”, juillet 2022.

On remarque ainsi que les classes les moins énergivores sont surreprésentées dans les données des DPE, contrairement aux logements ayant les étiquettes D et E. 

### Une base de données utile pour zoner et cartographier
Les données DPE permettent, notamment pour les collectivités locales, d’avoir une idée de l’état de leur parc de logement. Data.gouv.fr indique ainsi que l’un des usages qui peut être fait de ces bases de données ets le suivant : “Pour les acteurs publics qui souhaitent piloter leurs politiques publiques par la donnée : l'exploitation des données DPE permettrait de mieux caractériser le parc immobilier français, d'identifier les zones d'habitat indigne, de favoriser le recours à certains modes de consommation, etc.” (La base des diagnostics de performance énergétique (DPE) - data.gouv.fr. 2020. En ligne : https://www.data.gouv.fr/fr/posts/la-base-des-diagnostics-de-performance-energetique-dpe/ [consulté le 22 novembre 2022]). 

 Ce sont d’ailleurs des visualisations géographiques qui sont proposées en premier sur le site de l’Observatoire DPE. À partir de ces données, on peut par exemple réaliser une carte représentant le pourcentage de passoires thermiques par région avec les données des DPE établis depuis le 1er juillet 2022. 

![export](https://user-images.githubusercontent.com/115630234/203339992-2102ef2d-f283-48fd-a7c3-0c70f5a9394a.png)
Source : ADEME - Observatoire DPE (Diagnostic de Performance Énergétique). En ligne : https://observatoire-dpe.ademe.fr/statistiques/outil [consulté le 22 novembre 2022]. Traitement avec Magrit.

### Des usages prospectifs, en laissant notamment des acteurs privés ou des chercheurs s’emparer de ces données, avec opérations de valorisation ponctuelles
Du 11 au 22 juin 2020 a eu lieu le Hackathon RenovAction, dont le but était de laisser des développeurs travailler sur des projets de valorisation des données de l’ADEME, dont les DPE et trouver des solutions pour accompagner la rénovation énergétique. Certains projets présentés proposaient par exemple d’identifier sur un territoire le potentiel de rénovation, et faciliter la mise en relations des acteurs qui auraient besoin d’y être impliqués, par une cartographie de la performance énergétique des bâtiment, croisée avec le potentiel de rénovation de ces mêmes bâtiments, selon leurs caractéristiques.

### Bibliographie/Webographie
ADEME. DPE Logements existants (depuis juillet 2021). 2022. En ligne : https://data.ademe.fr/datasets/dpe-v2-logements-existants/full (consulté le 21 novembre 2022).

Freppel, Camille. 37,6 millions de logements en France au 1er janvier 2022 - Insee Focus - 279. 2022. En ligne : https://www.insee.fr/fr/statistiques/6653801 (consulté le 21 novembre 2022).

La base des diagnostics de performance énergétique (DPE) - data.gouv.fr. 2020. En ligne : https://www.data.gouv.fr/fr/posts/la-base-des-diagnostics-de-performance-energetique-dpe/ (consulté le 21 novembre 2022).

LOI n° 2010-788 du 12 juillet 2010 portant engagement national pour l’environnement (1).

Arrêté du 31 mars 2021 relatif aux méthodes et procédures applicables au diagnostic de performance énergétique et aux logiciels l’établissant.

ADEME - Observatoire DPE (Diagnostic de Performance Énergétique). En ligne : https://observatoire-dpe.ademe.fr/statistiques/outil (consulté le 21 novembre 2022).

Le parc de logements par classe de performance énergétique au 1er janvier 2022. En ligne : https://www.statistiques.developpement-durable.gouv.fr/le-parc-de-logements-par-classe-de-performance-energetique-au-1er-janvier-2022-0 (consulté le 21 novembre 2022).

L’Observatoire des diagnostics de performance énergétique – Ademe. En ligne : https://expertises.ademe.fr/batiment/chiffres-cles-observations/lobservatoire-diagnostics-performance-energetique (consulté le 21 novembre 2022).

Fichiers démographiques sur les logements et les individus | Insee. En ligne : https://www.insee.fr/fr/metadonnees/source/serie/s1019 (consulté le 21 novembre 2022).

ADEME - Observatoire DPE (Diagnostic de Performance Énergétique). En ligne : https://observatoire-dpe.ademe.fr/statistiques/outil (consulté le 21 novembre 2022).
