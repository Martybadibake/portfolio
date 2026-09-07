Déploiement d'une infrastructure MECM / SCCM
(Microsoft Endpoint Configuration Manager)

Contexte et objectif
Ce projet consiste en la mise en place complète d'une infrastructure SCCM (System Center Configuration Manager / MECM) en environnement de laboratoire, reproduisant les conditions d'un déploiement d'entreprise réel : de la préparation de l'Active Directory jusqu'au déploiement automatisé de systèmes d'exploitation et d'applications sur des postes clients.
L'objectif était de maîtriser un outil central de la gestion de parc informatique en entreprise, utilisé pour automatiser le déploiement d'OS, la gestion des applications, et l'administration centralisée de nombreux postes.

Technologies et outils utilisés
• Windows Server (Active Directory, DNS, DHCP, GPO)
• SQL Server (base de données SCCM)
• Microsoft Endpoint Configuration Manager (SCCM / MECM)
• VMware ESXi (virtualisation du lab)
• WDS (Windows Deployment Services) / PXE
• ADK + USMT (Assessment and Deployment Kit)
<img width="962" height="721" alt="001-Topology_network" src="https://github.com/user-attachments/assets/62d3ad6e-3d10-4a79-a081-918993161437" />

Étapes clés de la réalisation

1. Préparation de l'infrastructure de base
   
Configuration des commutateurs virtuels sur ESXi, création des VM Windows Server, mise en place d'une forêt Active Directory complète avec comptes, DNS, GPO et container SCCM dédié.<img width="1668" height="588" alt="002-Active-directory-sccm" src="https://github.com/user-attachments/assets/57fb7ff3-c31c-4b45-8d8e-abfe486b5854" />

<img width="1671" height="331" alt="003-dns-sccm" src="https://github.com/user-attachments/assets/026388b2-c265-40af-a061-780946a2c173" />

<img width="1680" height="405" alt="004-dhcp-sccm" src="https://github.com/user-attachments/assets/73bd50ce-73ce-421a-b2db-4aad0ab2960b" />

<img width="1666" height="402" alt="005-gpo-sccm" src="https://github.com/user-attachments/assets/709e77b4-786d-4008-8790-07e627696bee" />

2. Installation du site SCCM
   
Déploiement de la base SQL Server, extension du schéma Active Directory pour SCCM,installation de l'infrastructure et du site primaire SCCM.
<img width="1696" height="859" alt="006-sql-sccm" src="https://github.com/user-attachments/assets/cdb46647-fdfc-43cf-a1a6-4d6582431166" />

<img width="1576" height="590" alt="007-container-sccm" src="https://github.com/user-attachments/assets/17f60135-284a-41ab-ab7b-d87f74884e9d" />

<img width="1687" height="812" alt="008-Site-Primaire-sccm" src="https://github.com/user-attachments/assets/c3e014a8-cf67-4982-bd8b-721613179ece" />

3. Configuration de la hiérarchie SCCM
Mise en place des méthodes de découverte, des limites de site (Boundaries) et des groupes de limites pour une administration efficace du parc.

<img width="1642" height="834" alt="011-Groupe-Limites-sccm" src="https://github.com/user-attachments/assets/c2ae9b94-fcb4-4d5c-9b59-21231baddd41" />

<img width="1681" height="844" alt="009-Discovery-methode-sccm" src="https://github.com/user-attachments/assets/4ebfe47c-015b-43b4-a15f-159b2343cd58" />

<img width="1645" height="772" alt="010-Limite-sccm" src="https://github.com/user-attachments/assets/bc337eca-267e-45b4-b976-6967d3736e3d" />

4. Bonnes pratiques d'administration
Configuration du RBAC (contrôle d'accès basé sur les rôles), des composants de site, des rapports (Reporting Services), création de collections via requêtes SQL, et extension de l'infrastructure avec un second site (Management Point + Distribution Point).
<img width="1670" height="803" alt="014-Roles-securité-sccm" src="https://github.com/user-attachments/assets/a7eb275a-e6f6-416d-a44a-6bfd3ac86a3e" />

<img width="1690" height="900" alt="013-Rapports-sccm" src="https://github.com/user-attachments/assets/7cc9b8cc-b575-4342-87ee-3124d2b85d3a" />

<img width="1684" height="830" alt="013-02-utilisateurs-admin-sccm" src="https://github.com/user-attachments/assets/a6335ecf-3efc-4755-9a5e-6f601b19a4ff" />

<img width="1652" height="893" alt="012-Preripheriques-sccm" src="https://github.com/user-attachments/assets/b5c22735-81ac-45cb-b95c-097c80233537" />

<img width="1691" height="794" alt="012-02-Role-site-DP-secondaire" src="https://github.com/user-attachments/assets/415ec69a-78ea-430c-82f0-132bcf3a130b" />

<img width="1639" height="771" alt="012-01-Role-site-principale" src="https://github.com/user-attachments/assets/b165118b-5346-42de-8416-383d956778f5" />

5. Déploiement des agents clients
Installation et configuration des agents SCCM sur les postes, avec validation des prérequis.
<img width="1567" height="705" alt="015-Agent-clients-sccm" src="https://github.com/user-attachments/assets/32b33375-cd3a-447b-a2b0-045737c853ca" />

6. Gestion du cycle de vie des applications
Préparation des dépôts d'applications, création de packages (MSI/EXE), distribution vers les points de distribution, déploiement ciblé, supervision des déploiements et gestion des mises à jour de versions.
<img width="1437" height="810" alt="016-Distribution-logiciel-sur-client-sccm" src="https://github.com/user-attachments/assets/eeb8f757-0183-4205-a37d-a7bd8d5bbcfa" />
<img width="1629" height="969" alt="017-distribution-app-image-sccm" src="https://github.com/user-attachments/assets/e1f95df6-2f7b-48d2-9d44-fbdeca2bce58" />
<img width="1686" height="911" alt="018-App-exe-msi" src="https://github.com/user-attachments/assets/ab6b5fc1-5eea-4fed-86a9-3e6c65799bc2" />
<img width="1686" height="804" alt="019-Deploiement-app-sccm" src="https://github.com/user-attachments/assets/3d41c978-e587-44c7-9689-ab41bfe7976d" />
<img width="1693" height="790" alt="020-Deploiement-app-sccm" src="https://github.com/user-attachments/assets/2cb16487-22bb-4384-a5c1-b59c0b6186c9" />

7. Déploiement de systèmes d'exploitation (OSD)
Configuration du rôle WDS pour le PXE, gestion des images système (.WIM), création et déploiement de séquences de tâches (avec jonction automatique au domaine et à l'unité d'organisation appropriée), et configuration DHCP avancée (UEFI, Legacy, Vendor Class), Importation, packaging et intégration de pilotes matériels dans les séquences de déploiement pour assurer la compatibilité multi-matériel.
<img width="1016" height="770" alt="030-fin-intallation-w10" src="https://github.com/user-attachments/assets/f63b8d6b-55b7-44e8-9482-c5ccf2301a4f" />
<img width="1531" height="849" alt="031-Confirmation-app-distribuer-sur-client" src="https://github.com/user-attachments/assets/c8c4ce6b-b65a-4168-b4a0-fa77419ca32d" />
<img width="892" height="456" alt="029-Demarage-deployement" src="https://github.com/user-attachments/assets/96d6ff8e-acf6-46ae-9e83-e2cdb9931415" />
<img width="1740" height="880" alt="028-Reception-Client-PXE_w10" src="https://github.com/user-attachments/assets/c6cbc7be-75b2-42d3-a32e-0f784e19ddf8" />
<img width="1649" height="916" alt="023-Sequences-task" src="https://github.com/user-attachments/assets/88a26ae1-952b-47f1-93c7-f0d397ebc6ae" />
<img width="1662" height="942" alt="023-02-sequanceTask_sequences-sccm-28" src="https://github.com/user-attachments/assets/a452fc1a-a946-4ebd-9f43-da101ed2d142" />
<img width="1685" height="881" alt="022-Boot-image-sccm" src="https://github.com/user-attachments/assets/e19728ce-cb4d-4439-a246-7d10a76e4799" />

<img width="1508" height="854" alt="021-PXE-sccm" src="https://github.com/user-attachments/assets/cd52a56c-b379-4507-8b26-0c8af5600807" />
<img width="1693" height="790" alt="020-Deploiement-app-sccm" src="https://github.com/user-attachments/assets/04b7f799-3b76-4b50-89de-215aa56e5eb6" />
<img width="1686" height="804" alt="019-Deploiement-app-sccm" src="https://github.com/user-attachments/assets/213fd7d0-cb54-450d-90b9-eae1d6a7834e" />


<img width="1686" height="911" alt="018-App-exe-msi" src="https://github.com/user-attachments/assets/ee64c707-ecd4-4c4f-82a4-285170aada44" />






intégration de pilotes matériels dans les séquences de déploiement pour assurer la compatibilité multi-matériel.

