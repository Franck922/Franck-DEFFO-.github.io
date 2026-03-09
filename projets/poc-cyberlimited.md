# 🛡️ POC "Cyber Limited" : Conception & Durcissement d'une Infrastructure Sécurisée
> Projet de Sécurisation Multi-Systèmes | Keyce Academy | Avril 2025

---
### 📄 [Consulter le Rapport Technique (PDF)](../Rapport atelier 2.docx - Google Docs.pdf)
---

## 📝 Contexte du Projet
L'objectif était de concevoir, déployer et sécuriser l'infrastructure complète d'une entreprise fictive nommée **Cyber Limited**. Ce Proof of Concept (POC) simule un environnement de production où chaque machine doit être protégée contre les intrusions et les attaques réseau.

## 🏗️ Architecture du Lab (Virtualisation VMware)
L'environnement est composé de 5 machines virtuelles isolées dans un réseau sécurisé (VMnet2) :
*   **pfSense** : Pare-feu central et passerelle sécurisée.
*   **Ubuntu Server** : Hébergement de services critiques et de l'IDS.
*   **Windows Server 2019** : Contrôleur de domaine et gestion des politiques (GPO).
*   **Postes Clients (Win10 & Ubuntu)** : Simulation d'environnements utilisateurs.

## 🛠️ Réalisations Techniques & Sécurité

### 1. Sécurité Réseau avec pfSense
*   **Installation & Configuration** : Mise en place du filtrage de paquets, gestion des interfaces LAN/WAN et isolation du réseau interne.
*   **Politiques de filtrage** : Blocage systématique des flux entrants non sollicités et contrôle strict du trafic ICMP.

### 2. Détection d'Intrusions avec Snort (IDS)
*   **Déploiement** : Installation de **Snort** sur Ubuntu Server pour l'analyse du trafic en temps réel.
*   **Règles personnalisées** : Création de règles de détection (ex: alertes ICMP) et validation de la configuration via tests de pénétration. [Rapport page 13](/knowledge-base/pdf/Rapport%20atelier%202.docx%20-%20Google%20Docs?page=13).

### 3. Durcissement des Systèmes (System Hardening)
Application des meilleures pratiques de sécurité sur chaque OS :
*   **Linux (Ubuntu)** : Activation de **UFW**, installation de **Fail2ban** contre les attaques brute force SSH, et suppression des services inutiles.
*   **Windows** : Mise en œuvre de stratégies de groupe (**GPO**), configuration du Pare-feu Avancé et gestion rigoureuse des privilèges locaux. [Rapport page 18](/knowledge-base/pdf/Rapport%20atelier%202.docx%20-%20Google%20Docs?page=18).

## 🛡️ Tests de Sécurité (Pentest de validation)
Pour valider l'infrastructure, j'ai réalisé des tests d'intrusion simulés :
*   **Scans de ports (Nmap)** : Vérification de la discrétion des services.
*   **Attaques par force brute** : Test de l'efficacité de Fail2ban et des politiques de verrouillage de comptes.
*   **Ping Floods** : Test de la résistance du réseau face au déni de service.

## ✅ Résultats
*   Une infrastructure 100% isolée et résistante aux attaques courantes.
*   Mise en place d'une visibilité complète sur les alertes réseau via l'IDS Snort.
*   Documentation complète des procédures de durcissement reproductibles.

---
[⬅️ Retour à l'accueil](../README.md)
