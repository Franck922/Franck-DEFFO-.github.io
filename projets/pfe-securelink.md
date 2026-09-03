---
layout: default
title: SecureLink — Détection de Phishing par IA
---

<div class="project-detail">

<span class="card-label">Projet de Fin d'Études · Octobre 2025 – Mars 2026 · ECE Paris</span>

<h1>🛡️ SecureLink : Plateforme Intelligente de Détection de Phishing</h1>

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
