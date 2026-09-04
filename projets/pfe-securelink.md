---
layout: default
title: SecureLink — Détection de Phishing par IA
---

<div class="project-detail">

<span class="card-label">Projet de Fin d'Études · Octobre 2025 – Mars 2026 · ECE Paris</span>

<h1>🛡️ SecureLink : Plateforme Intelligente de Détection de Phishing</h1>

<div style="margin-bottom: 2rem;">
  <a href="https://github.com/Franck922/SecureLink-Phishing-Detection" target="_blank" style="display: inline-flex; align-items: center; gap: 0.5rem; background: #1e293b; color: white; padding: 0.5rem 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
    <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    Voir le code source sur GitHub
  </a>
</div>

<div class="card-tags">
    <span class="card-tag">JavaScript</span>
    <span class="card-tag">React 19</span>
    <span class="card-tag--purple card-tag">FastAPI</span>
    <span class="card-tag--purple card-tag">MongoDB</span>
    <span class="card-tag--cyan card-tag">Machine Learning</span>
    <span class="card-tag--cyan card-tag">scikit-learn</span>
</div>

<h2>🎯 Contexte et Objectifs</h2>

<p>Face à l'augmentation des violations de données (dont 15% impliquent une faille humaine selon le rapport Verizon DBIR 2025), le défi était de concevoir un outil de sécurité avec <strong>zéro friction pour l'utilisateur final</strong>. SecureLink permet d'analyser un lien suspect en un clic, tout en combinant une approche grand public (acculturation et e-learning) avec une sécurisation robuste pour les entreprises.</p>

<h2>⚙️ Architecture Technique : Asynchronisme et Modularité</h2>

<p>L'exigence principale du système était la <strong>dégradation gracieuse</strong>. Le backend ne devait jamais bloquer l'analyse même si une API externe devenait indisponible.</p>

<ul>
    <li><strong>Frontend :</strong> Interface moderne, dynamique et "zéro friction" développée en <strong>JavaScript / React 19</strong> avec TailwindCSS. L'utilisateur analyse son lien sans processus complexe d'inscription.</li>
    <li><strong>Backend :</strong> API Asynchrone sous <strong>FastAPI</strong> (Python). Le choix de l'asynchrone permet d'orchestrer les requêtes vers les 12 couches d'analyse sans blocage du thread principal.</li>
    <li><strong>Base de Données :</strong> Utilisation de <strong>MongoDB</strong> (NoSQL documentaire) pour stocker les résultats d'analyses, idéal pour gérer les formats JSON variables renvoyés par les API d'inspection de contenu.</li>
    <li><strong>Défis résolus :</strong> La gestion du timeout des APIs (ex: WHOIS) par continuation sans blocage, et l'isolation des processus (Subprocess) pour éviter les crashs de requêtes sur les environnements Windows.</li>
</ul>

<h2>🧠 Le Moteur Hybride à 12 Couches</h2>

<p>La force de SecureLink repose sur son moteur de scoring hybride qui élimine les faux positifs :</p>

<ul>
    <li><strong>Modèle Machine Learning (35%) :</strong> Algorithme <em>Random Forest</em> entraîné sur 20 caractéristiques (features) pour identifier les schémas comportementaux du phishing.</li>
    <li><strong>Règles Métier & Algorithmes (20%) :</strong> Détection du typosquattage (ex: homoglyphes Unicode) par distance de Levenshtein et table de substitution ciblée.</li>
    <li><strong>Vérifications Réseau & Contenu (45%) :</strong> Inspection du certificat SSL/TLS, analyse DNS, et vérification des formulaires suspects en direct.</li>
</ul>

<blockquote>
    <strong>💡 Innovation "Boost de Légitimité" :</strong> Pour contrer les faux positifs sur des sites complexes, nous avons intégré un mécanisme de compensation empirique (Grid Search) qui redescend le score de dangerosité si le domaine est structurellement validé.
</blockquote>

<h2>📈 Résultats et Impact</h2>

<p>La validation empirique du modèle a été réalisée sur un benchmark de <strong>74 URLs réelles</strong> (45 sites légitimes, 29 sites de phishing avérés).</p>

<div class="card-result">✅ <strong>Précision (Precision) :</strong> 100%</div>
<div class="card-result">✅ <strong>Rappel (Recall) :</strong> 100%</div>
<div class="card-result">✅ <strong>Accuracy / F1-Score :</strong> 100% — 0 faux positif, 0 faux négatif</div>

<p><strong>Conclusion :</strong> La suprématie de l'approche hybride pondérée (combiner ML local et règles heuristiques) permet non seulement d'atteindre des métriques parfaites en laboratoire, mais aussi de proposer une solution commerciale viable (modèle Freemium avec API dédiées aux Grands Comptes).</p>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
