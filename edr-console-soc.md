---
layout: default
title: Détecteur Hybride de Rançongiciels (EDR & SOC)
---

# 🛡️ Infrastructure EDR & Console SOC : Détection de Rançongiciels

> **Projet de Substitution au Stage (Opérationnel)** | Juillet - Août 2026 | ECE Paris

<p align="center">
  <img src="https://img.shields.io/badge/Windows_Server-0078D6?style=for-the-badge&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=FastAPI&logoColor=white" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
</p>

## 🎯 Contexte et Objectifs

Les rançongiciels (ransomwares) figurent parmi les menaces les plus destructrices pour les organisations modernes. Face à l'inefficacité des antivirus traditionnels (basés sur des signatures) contre les variantes polymorphes, l'objectif de ce projet était de concevoir et déployer une plateforme EDR (Endpoint Detection and Response) complète, du capteur sur le poste de travail jusqu'à la console métier pour les analystes SOC.

## ⚙️ Architecture Technique & Maintien en Conditions Opérationnelles

Le projet repose sur une architecture robuste, capable de résister aux attaques simulées sans compromettre le réseau hôte (laboratoire confiné sous VMware).

- **Collecte de Télémetrie Windows :** Déploiement de **Sysmon** et **Winlogbeat** pour capturer des événements spécifiques à très forte valeur ajoutée (création massive de fichiers, entropie anormale, tentatives de suppression de clichés VSS).
- **Détection Hybride :** Conception d'un pipeline Python capable de normaliser les journaux Elastic (Winlogbeat) et de calculer des z-scores en temps réel par rapport à la "baseline" comportementale de la machine.
- **Réponse Active (Agent PowerShell) :** Développement d'un agent léger interrogeant l'API pour récupérer et exécuter des ordres d'isolation réseau (via Windows Firewall) ou d'arrêt de processus malveillants.
- **Console SOC Multi-Analystes :** Architecture conteneurisée (Docker Compose) incluant **PostgreSQL 16**, une API **FastAPI** et un frontend **React/TailwindCSS**. La console permet à plusieurs analystes de superviser le parc simultanément, avec gestion stricte des sessions, authentification (Argon2id) et droits d'accès.

## 🚀 AMOA et Documentation

En parallèle du développement, un accent majeur a été mis sur la qualité, la traçabilité et le transfert de compétences, éléments clés dans le pilotage d'un projet industriel :
1. **Tests E2E automatisés :** Création d'une suite de 86 contrôles automatisés garantissant le bon fonctionnement de l'ingestion, de l'authentification et de la riposte.
2. **Gestion d'Audit :** Implémentation d'un journal d'audit infalsifiable côté serveur pour tracer les actions des analystes (qui a déclenché l'arrêt de quel processus).
3. **Livraison d'un Guide de Reproduction :** Rédaction d'une documentation exhaustive permettant à un non-développeur de rejouer l'ensemble des attaques et des détections, démontrant ma capacité à vulgariser et documenter des systèmes complexes.

## 📈 Résultats et Impact

La solution a été testée contre un simulateur inoffensif reproduisant des techniques réelles du framework **MITRE ATT&CK** (T1071, T1490, T1486).

*   **Vitesse d'intervention :** Détection, confirmation (par le modèle de Machine Learning / Moteur de règles) et arrêt du processus malveillant en **quelques secondes**.
*   **Qualité logicielle :** La migration finale vers PostgreSQL a résolu les problèmes de concurrence initiaux, prouvant ma capacité à adapter une architecture face à des problèmes de montée en charge.

---
[⬅️ Retour à l'accueil](../README.md)
