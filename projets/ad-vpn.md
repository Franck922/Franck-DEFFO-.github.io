# 🔐 TechSecure : Architecture Active Directory & VPN à Certificats
> Projet Infrastructure & Sécurité | ECE Paris

## 📝 Objectif du Projet
Concevoir et déployer une infrastructure d'entreprise sécurisée ("TechSecure") capable de centraliser la gestion des identités et de permettre un accès distant hautement sécurisé pour les collaborateurs nomades.

## 🏗️ Architecture du Réseau
L'infrastructure repose sur un réseau interne isolé ("intnet") garantissant que les serveurs critiques ne sont jamais exposés directement sur Internet sans protection.
*   **Contrôleur de Domaine** : Windows Server 2019 (AD DS, DNS, DHCP).
*   **Passerelle VPN** : Serveur Linux Ubuntu durci.
*   **Clients** : Postes Windows 10 intégrés au domaine.

## 🛠️ Réalisations Techniques

### 1. Administration Active Directory (AD DS)
*   **Gestion des Identités** : Création d'une structure d'Unités d'Organisation (OU) par services : **RH, Technique, Comptabilité, Direction**.
*   **Gouvernance via GPO** : Mise en œuvre de stratégies de groupe pour restreindre les privilèges locaux, imposer des politiques de mots de passe forts et assurer la traçabilité des logs.
*   **Audit de Conformité** : Vérification de la cohérence des droits d'accès en accord avec le principe du moindre privilège.

### 2. Sécurisation des Accès Distants (VPN PKI)
*   **Déploiement d'OpenVPN** : Installation et configuration d'un tunnel sécurisé pour l'interconnexion des clients distants au LAN de l'entreprise.
*   **Mise en place d'une PKI (Easy-RSA)** : Génération d'une Autorité de Certification (CA) interne pour la signature des certificats clients X.509.
*   **Authentification par Certificats** : Remplacement de l'authentification simple par une authentification forte basée sur des certificats numériques, garantissant l'intégrité et la confidentialité des flux.

### 🛡️ Sécurité & Étanchéité Réseau
*   **Segmentation** : Isolation des serveurs de base de données via des règles de filtrage.
*   **Hardening** : Désactivation des services inutiles et durcissement des configurations réseau sur le serveur VPN.

## ✅ Résultats Obtenus
*   Infrastructure robuste et évolutive permettant une administration centralisée.
*   Accès distant opérationnel, testé et validé par certificats, offrant le même niveau de sécurité qu'au bureau.
*   Conformité aux bonnes pratiques de cybersécurité en matière de gestion des identités et des accès (IAM).

---
[⬅️ Retour à l'accueil](../README.md)
