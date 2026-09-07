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

4. Configuration de la hiérarchie SCCM
Mise en place des méthodes de découverte, des limites de site (Boundaries) et des groupes de limites pour une administration efficace du parc.

5. Bonnes pratiques d'administration
Configuration du RBAC (contrôle d'accès basé sur les rôles), des composants de site, des rapports (Reporting Services), création de collections via requêtes SQL, et extension de l'infrastructure avec un second site (Management Point + Distribution Point).

6. Déploiement des agents clients
Installation et configuration des agents SCCM sur les postes, avec validation des prérequis.

7. Gestion du cycle de vie des applications
Préparation des dépôts d'applications, création de packages (MSI/EXE), distribution vers les points de distribution, déploiement ciblé, supervision des déploiements et gestion des mises à jour de versions.

8. Déploiement de systèmes d'exploitation (OSD)
Configuration du rôle WDS pour le PXE, gestion des images système (.WIM), création et déploiement de séquences de tâches (avec jonction automatique au domaine et à l'unité d'organisation appropriée), et configuration DHCP avancée (UEFI, Legacy, Vendor Class).

9. Intégration des pilotes (drivers)
Importation, packaging et intégration de pilotes matériels dans les séquences de déploiement pour assurer la compatibilité multi-matériel.

Compétences démontrées
• Conception et déploiement d'une infrastructure Windows Server complète (AD, DNS, DHCP, GPO)
• Administration d'un outil de gestion de parc informatique à l'échelle entreprise
• Automatisation du déploiement d'OS et d'applications
• Résolution de problématiques réseau (PXE, DHCP multi-scénarios)
• Compréhension des architectures multi-sites (MP/DP)

















