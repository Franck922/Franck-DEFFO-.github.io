---
layout: default
title: Infrastructure EDR & Console SOC
---

<div class="project-detail">

<span class="card-label card-label--purple">Projet Opérationnel (Substitution) · Juillet – Août 2026 · ECE Paris</span>

<h1>🛡️ Infrastructure EDR & Console SOC : Détection de Rançongiciels</h1>

<div class="card-tags">
    <span class="card-tag">Windows Server</span>
    <span class="card-tag--purple card-tag">PowerShell</span>
    <span class="card-tag--purple card-tag">PostgreSQL</span>
    <span class="card-tag">Docker</span>
    <span class="card-tag--cyan card-tag">FastAPI</span>
    <span class="card-tag--cyan card-tag">React</span>
</div>

<h2>🎯 Contexte et Objectifs</h2>

<p>Les rançongiciels (ransomwares) figurent parmi les menaces les plus destructrices pour les organisations modernes. Face à l'inefficacité des antivirus traditionnels (basés sur des signatures) contre les variantes polymorphes, l'objectif de ce projet était de concevoir et déployer une plateforme EDR (Endpoint Detection and Response) complète, du capteur sur le poste de travail jusqu'à la console métier pour les analystes SOC.</p>

<h2>⚙️ Architecture Technique & Maintien en Conditions Opérationnelles</h2>

<p>Le projet repose sur une architecture robuste, capable de résister aux attaques simulées sans compromettre le réseau hôte (laboratoire confiné sous VMware).</p>

<ul>
    <li><strong>Collecte de Télémetrie Windows :</strong> Déploiement de <strong>Sysmon</strong> et <strong>Winlogbeat</strong> pour capturer des événements spécifiques à très forte valeur ajoutée (création massive de fichiers, entropie anormale, tentatives de suppression de clichés VSS).</li>
    <li><strong>Détection Hybride :</strong> Conception d'un pipeline Python capable de normaliser les journaux Elastic (Winlogbeat) et de calculer des z-scores en temps réel par rapport à la "baseline" comportementale de la machine.</li>
    <li><strong>Réponse Active (Agent PowerShell) :</strong> Développement d'un agent léger interrogeant l'API pour récupérer et exécuter des ordres d'isolation réseau (via Windows Firewall) ou d'arrêt de processus malveillants.</li>
    <li><strong>Console SOC Multi-Analystes :</strong> Architecture conteneurisée (Docker Compose) incluant <strong>PostgreSQL 16</strong>, une API <strong>FastAPI</strong> et un frontend <strong>React/TailwindCSS</strong>. La console permet à plusieurs analystes de superviser le parc simultanément, avec gestion stricte des sessions, authentification (Argon2id) et droits d'accès.</li>
</ul>

<h2>🚀 AMOA et Documentation</h2>

<p>En parallèle du développement, un accent majeur a été mis sur la qualité, la traçabilité et le transfert de compétences :</p>

<ul>
    <li><strong>Tests E2E automatisés :</strong> Création d'une suite de 86 contrôles automatisés garantissant le bon fonctionnement de l'ingestion, de l'authentification et de la riposte.</li>
    <li><strong>Gestion d'Audit :</strong> Implémentation d'un journal d'audit infalsifiable côté serveur pour tracer les actions des analystes (qui a déclenché l'arrêt de quel processus).</li>
    <li><strong>Livraison d'un Guide de Reproduction :</strong> Rédaction d'une documentation exhaustive permettant à un non-développeur de rejouer l'ensemble des attaques et des détections.</li>
</ul>

<h2>📈 Résultats et Impact</h2>

<p>La solution a été testée contre un simulateur inoffensif reproduisant des techniques réelles du framework <strong>MITRE ATT&CK</strong> (T1071, T1490, T1486).</p>

<div class="card-result">⚡ Détection et blocage du processus malveillant en <strong>quelques secondes</strong></div>
<div class="card-result">✅ <strong>F1-score de 1.00</strong> sur un jeu de données de 14 800+ événements</div>
<div class="card-result">🧪 <strong>86 tests End-to-End</strong> automatisés pour garantir la qualité logicielle</div>

<p><strong>Conclusion :</strong> La migration finale vers PostgreSQL a résolu les problèmes de concurrence initiaux, prouvant ma capacité à adapter une architecture face à des problèmes de montée en charge. L'approche "documentation-first" garantit la pérennité et la maintenabilité de la solution.</p>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
