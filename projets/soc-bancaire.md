# 🏦 Mise en place d’un SOC et Supervision d’une Infrastructure Bancaire
> Projet réalisé à l'ECE Paris | Février - Mars 2026

## 📝 Contexte du Projet
Dans le secteur bancaire, la disponibilité des services et la confidentialité des données financières sont critiques. Ce projet consistait à simuler une infrastructure bancaire complète et à déployer un **SOC (Security Operations Center)** pour surveiller, détecter et réagir aux incidents en temps réel.

## 🏗️ Architecture Technique
L'infrastructure est composée de 5 machines virtuelles interconnectées, simulant un environnement d'entreprise réel :
*   **Poste Windows** : Simulant un employé de banque (génération de logs utilisateur).
*   **Serveur Web (Apache)** : Application bancaire accessible aux clients.
*   **Serveur DB (MySQL)** : Base de données critique contenant les transactions.
*   **Poste Admin (Linux)** : Machine d'administration et de test de sécurité.
*   **Serveur SOC (AlmaLinux)** : Centre de supervision hébergeant la stack technique.

## 🛠️ Stack Technologique (Outils Industriels)
*   **SIEM** : **Wazuh** pour l'analyse des journaux et la détection d'intrusions.
*   **Monitoring** : **Zabbix** pour la surveillance de la santé des serveurs (CPU, RAM, ports).
*   **Dashboarding** : **Grafana** pour la corrélation et la visualisation dynamique des alertes.

## 🛡️ Réalisations & Tests de Sécurité
Pour valider l'efficacité du SOC, j'ai simulé et analysé plusieurs attaques réelles :

### 1. Détection d'Attaque Brute Force SSH
*   **Action** : Simulation de tentatives de connexion répétées sur le serveur d'administration.
*   **Résultat** : Wazuh a identifié le comportement suspect, corrélé les échecs d'authentification et généré une alerte de niveau critique.

### 2. Surveillance d'Intégrité des Fichiers (FIM)
*   **Action** : Modification non autorisée de fichiers système critiques dans `/etc/`.
*   **Résultat** : Détection instantanée via le module **FIM de Wazuh**, rapportant l'heure exacte et l'utilisateur ayant effectué l'action.

### 3. Monitoring de Disponibilité & Performance
*   **Action** : Configuration d'agents Zabbix pour surveiller l'état des services Apache et MySQL.
*   **Résultat** : Création de tableaux de bord Grafana permettant d'anticiper les pannes et de visualiser l'état du parc en un coup d'œil.

## 🚀 Difficultés Résolues
*   **Conflits d'identifiants** : Résolution de problèmes liés au clonage de VM causant des doublons d'agents Wazuh.
*   **Diagnostic de communication** : Utilisation de `zabbix_get` pour débugger les flux entre le serveur et les agents isolés.

---
[⬅️ Retour à l'accueil](../README.md)
