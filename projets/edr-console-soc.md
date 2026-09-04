---
layout: default
title: Infrastructure EDR & Console SOC
---

<div class="project-detail">

<span class="card-label card-label--purple">Projet Opérationnel (Substitution) · Juillet – Août 2026 · ECE Paris</span>

<h1>🛡️ Infrastructure EDR & Console SOC : Détection de Rançongiciels</h1>

<div style="margin-bottom: 2rem;">
  <a href="https://github.com/Franck922/ransomware-detector" target="_blank" style="display: inline-flex; align-items: center; gap: 0.5rem; background: #1e293b; color: white; padding: 0.5rem 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
    <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    Voir le code source sur GitHub
  </a>
</div>

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
