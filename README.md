# 🛡️ Franck DEFFO | Portfolio Ingénierie Cybersécurité & Réseaux
> *Étudiant Bachelor 3 ECE Paris | Junior Cybersecurity Analyst (Cisco Certified)*

Bienvenue sur ma plateforme de réalisations techniques. Ce portfolio est conçu comme une documentation vivante de mes compétences opérationnelles. De la conception d'architectures réseaux résilientes à la mise en œuvre de centres de surveillance (SOC), chaque projet ici démontre une capacité à résoudre des problématiques complexes de sécurité et d'infrastructure.

---

## 🚀 Projets Majeurs & Études de Cas

### 🏦 [SOC & Supervision : Infrastructure Bancaire Critique](./projets/soc-bancaire.md)
*   **Objectif** : Garantir la disponibilité et la détection d'intrusions sur un environnement bancaire simulé (5 VM).
*   **Expertise technique** : 
    *   Déploiement du SIEM **Wazuh** avec activation du **FIM** (File Integrity Monitoring) pour la surveillance des fichiers `/etc/`.
    *   Supervision proactive via **Zabbix** (Monitoring CPU/RAM/Services) et corrélation de données avec **Grafana**.
    *   **Détection active** : Analyse et blocage d'attaques **Brute Force SSH** et de requêtes HTTP malveillantes.
*   **Résultat** : Visibilité 360° sur l'état de sécurité et réduction drastique du temps de détection.

### 🔐 [TechSecure : Architecture Active Directory & VPN PKI](./projets/ad-vpn.md)
*   **Objectif** : Créer une infrastructure d'entreprise sécurisée pour le travail nomade.
*   **Expertise technique** : 
    *   Administration de **Windows Server 2019** : Configuration de l'annuaire **AD DS**, DNS et mise en œuvre de **GPO** restrictives.
    *   Sécurisation des accès : Tunnel **OpenVPN** avec authentification forte basée sur une **PKI (Easy-RSA)** et certificats X.509.
    *   Isolation réseau : Mise en place de l'étanchéité entre le réseau interne ("intnet") et les accès externes.
*   **Résultat** : Un environnement centralisé, conforme aux bonnes pratiques de gestion des identités.

### 🛡️ [Analyse de Menaces : Frameworks MITRE ATT&CK & D3FEND](./projets/mitre-analyse.md)
*   **Objectif** : Modéliser le mode opératoire des attaquants pour définir des stratégies de défense.
*   **Expertise technique** : 
    *   Étude du scénario **SCADA** (Réseau industriel) : Analyse des tactiques de mouvement latéral et d'exfiltration.
    *   Mapping offensif : Identification des techniques (TTPs) comme l'exploitation de failles Kernel pour l'escalade de privilèges.
    *   Réponse défensive : Préconisation de contre-mesures via **MITRE D3FEND** (Segmentation, durcissement des identifiants).
*   **Résultat** : Rapport de remédiation structuré pour infrastructures critiques.

---

## 🌐 Bibliothèque de Travaux Pratiques (Expertise Réseaux)

### 🛰️ [Ingénierie Réseaux Cisco & IPv6 Avancé](./projets/tp-reseaux-ipv6.md)
*   **Concepts clés** : Dual-Stack (IPv4/IPv6), Autoconfiguration **SLAAC**, Routage statique & dynamique (**OSPF**).
*   **Réalisation** : Calcul et déploiement d'un plan d'adressage **VLSM** pour 4 LANs hétérogènes, optimisant l'espace d'adressage de 40%.

### 🏗️ [Commutation & Sécurisation LAN](./projets/tp-vlan-stp.md)
*   **Concepts clés** : **VLAN**, **Trunking (802.1Q)**, **VTP**, **Spanning Tree (STP)**.
*   **Réalisation** : Configuration d'une topologie redondante avec propagation automatique des VLANs et sécurisation des accès distants via **SSHv2**.

### 🔒 [Sécurisation des Flux : VPN IPsec Site-à-Site](./projets/tp-vpn-ipsec.md)
*   **Concepts clés** : Cryptographie (AES/SHA), ISAKMP, Transform Sets, ACLs.
*   **Réalisation** : Interconnexion sécurisée de deux sites distants via un tunnel de chiffrement industriel sur routeurs Cisco.

---

## 🐧 Systèmes, Virtualisation & Services

### 📂 [Gestion d'Annuaire & Authentification](./projets/tp-ldap-auth.md)
*   **Travaux** : Mise en œuvre d'**OpenLDAP** sous Linux, gestion des Unités Organisationnelles et analyse des journaux d'erreurs d'authentification pour la détection de comportements suspects.

### 🕸️ [Virtualisation & Services Web](./projets/tp-virtualisation-apache.md)
*   **Travaux** : Configuration de routeurs Linux sous **VMware**, sécurisation de serveurs **Apache2** et diagnostic réseau via **Netcat** (Reverse Shell analysis).

---

## 📜 Certifications & Formations

*   🎓 **Bachelor 3 Cybersécurité & Réseaux** – ECE Paris
*   🏆 **Cisco Certified** : Junior Cybersecurity Analyst, Cyber Threat Management, Network Defense.
*   🛡️ **ANSSI** : Certifié SecNumacadémie (Expertise SSI France).
*   📊 **DataScientest** : Certifié Tech Away Cyber niv2 (Sécurité Opérationnelle).

---

📬 **Contact professionnel :**
[LinkedIn](https://www.linkedin.com/in/franck-deffo) | [GitHub](https://github.com/Franck922) | [Email](mailto:franckdeffo12@gmail.com)
