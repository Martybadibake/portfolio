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
• ADK + USMT (Assessment and Deployment Kit)<img width="962" height="721" alt="001-Topology_network" src="https://github.com/user-attachments/assets/69db7b6f-e19c-4c17-a437-984850afd94d" />


Étapes clés de la réalisation

1. Préparation de l'infrastructure de base
Configuration des commutateurs virtuels sur ESXi, création des VM Windows Server, mise en place d'une forêt Active Directory complète avec comptes, DNS, GPO et container SCCM dédié.

2. Installation du site SCCM
Déploiement de la base SQL Server, extension du schéma Active Directory pour SCCM, installation de l'infrastructure et du site primaire SCCM.

3. Configuration de la hiérarchie SCCM
Mise en place des méthodes de découverte, des limites de site (Boundaries) et des groupes de limites pour une administration efficace du parc.

4. Bonnes pratiques d'administration<img width="1666" height="402" alt="005-gpo-sccm" src="https://github.com/user-attachments/assets/d3ced827-0c39-4181-a740-17965ced5fa7" />
<img width="1680" height="405" alt="004-dhcp-sccm" src="https://github.com/user-attachments/assets/1a82e36f-64cb-45a6-9a9b-c75e05014c98" />
<img width="1671" height="331" alt="003-dns-sccm" src="https://github.com/user-attachments/assets/f6deda92-208a-455e-ab1c-3d170e5f1811" />
<img width="1668" height="588" alt="002-Active-directory-sccm" src="https://github.com/user-attachments/assets/fb5e8135-e0a3-42ae-90a9-c2317ec94eb5" />
n
Configuration du RBAC (contrôle d'accès basé sur les rôles), des composants de site, des rapports (Reporting Services), création de collections via requêtes SQL, et extension de l'infrastructure avec un second site (Management Point + Distribution Point).

5. Déploiement des agents clients
Installation et configuration des agents SCCM sur les postes, avec validation des prérequis.

6. Gestion du cycle de vie des applications
Préparation des dépôts d'applications, création de packages (MSI/EXE), distribution vers les points de distribution, déploiement ciblé, supervision des déploiements et gestion des mises à jour de versions.

7. Déploiement de systèmes d'exploitation (OSD)
Configuration du rôle WDS pour le PXE, gestion des images système (.WIM), création et déploiement de séquences de tâches (avec jonction automatique au domaine et à l'unité d'organisation appropriée), et configuration DHCP avancée (UEFI, Legacy, Vendor Class).

8. Intégration des pilotes (drivers)
Importation, packaging et intégration de pilotes matériels dans les séquences de déploiement pour assurer la compatibilité multi-matériel.

Compétences démontrées
• Conception et déploiement d'une infrastructure Windows Server complète (AD, DNS, DHCP, GPO)
• Administration d'un outil de gestion de parc informatique à l'échelle entreprise
• Automatisation du déploiement d'OS et d'applications
• Résolution de problématiques réseau (PXE, DHCP multi-scénarios)
• Compréhension des architectures multi-sites (MP/DP)

















