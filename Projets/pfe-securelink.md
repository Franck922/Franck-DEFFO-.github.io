---
layout: default
title: SecureLink - Détection de Phishing par IA
---

# 🛡️ SecureLink : Plateforme Intelligente de Détection de Phishing

> **Projet de Fin d'Études (PFE)** | Octobre 2025 - Mars 2026 | ECE Paris

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=FastAPI&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Machine_Learning-FF6F00?style=for-the-badge&logo=scikit-learn&logoColor=white" />
</p>

## 🎯 Contexte et Objectifs

Face à l'augmentation des violations de données (dont 15% impliquent une faille humaine selon le rapport Verizon DBIR 2025), le défi était de concevoir un outil de sécurité avec **zéro friction pour l'utilisateur final**. SecureLink permet d'analyser un lien suspect en un clic, tout en combinant une approche grand public (acculturation et e-learning) avec une sécurisation robuste pour les entreprises.

## ⚙️ Architecture Technique : Asynchronisme et Modularité

L'exigence principale du système était la **dégradation gracieuse**. Le backend ne devait jamais bloquer l'analyse même si une API externe devenait indisponible.

- **Frontend :** Interface moderne, dynamique et "zéro friction" développée en **JavaScript / React 19** avec TailwindCSS. L'utilisateur analyse son lien sans processus complexe d'inscription.
- **Backend :** API Asynchrone sous **FastAPI** (Python). Le choix de l'asynchrone permet d'orchestrer les requêtes vers les 12 couches d'analyse sans blocage du thread principal.
- **Base de Données :** Utilisation de **MongoDB** (NoSQL documentaire) pour stocker les résultats d'analyses, idéal pour gérer les formats JSON variables renvoyés par les API d'inspection de contenu.
- **Défis résolus :** La gestion du timeout des APIs (ex: WHOIS) par continuation sans blocage, et l'isolation des processus (Subprocess) pour éviter les crashs de requêtes sur les environnements Windows.

## 🧠 Le Moteur Hybride à 12 Couches

La force de SecureLink repose sur son moteur de scoring hybride qui élimine les faux positifs :
1. **Modèle Machine Learning (35%) :** Algorithme *Random Forest* entraîné sur 20 caractéristiques (features) pour identifier les schémas comportementaux du phishing.
2. **Règles Métier & Algorithmes (20%) :** Détection du typosquattage (ex: homoglyphes Unicode) par distance de Levenshtein et table de substitution ciblée.
3. **Vérifications Réseau & Contenu (45%) :** Inspection du certificat SSL/TLS, analyse DNS, et vérification des formulaires suspects en direct.

> [!TIP]
> **Innovation "Boost de Légitimité" :** Pour contrer les faux positifs sur des sites complexes (qui déclenchent souvent des alertes heuristiques erronées), nous avons intégré un mécanisme de compensation empirique (Grid Search) qui redescend le score de dangerosité si le domaine est structurellement validé.

## 📈 Résultats et Impact

La validation empirique du modèle a été réalisée sur un benchmark de **74 URLs réelles** (45 sites légitimes, 29 sites de phishing avérés). 

*   **Précision (Precision) :** 100%
*   **Rappel (Recall) :** 100%
*   **Accuracy / F1-Score :** 100% (0 faux positif, 0 faux négatif sur le dataset de validation).

**Conclusion :** La suprématie de l'approche hybride pondérée (combiner ML local et règles heuristiques) permet non seulement d'atteindre des métriques parfaites en laboratoire, mais aussi de proposer une solution commerciale viable (modèle Freemium avec API dédiées aux Grands Comptes).

---
[⬅️ Retour à l'accueil](../README.md)
