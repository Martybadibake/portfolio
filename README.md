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





