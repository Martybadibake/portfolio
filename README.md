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









