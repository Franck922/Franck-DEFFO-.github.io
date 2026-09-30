---
layout: default
title: Pilotage agile et sécurisation applicative
description: Structuration en sprints, planification Gantt, stratégie d'authentification et audit OWASP Top 10 sur une plateforme de streaming.
---

<div class="project-detail">

<span class="card-label card-label--cyan">Pilotage · Sécurité applicative · NOV à DÉC 2025</span>

<h1>📋 Pilotage agile et sécurisation applicative</h1>

<div class="card-tags">
    <span class="card-tag card-tag--cyan">Scrum</span>
    <span class="card-tag card-tag--cyan">Jira</span>
    <span class="card-tag card-tag--cyan">Gantt</span>
    <span class="card-tag card-tag--cyan">OWASP Top 10</span>
    <span class="card-tag card-tag--cyan">JWT</span>
    <span class="card-tag card-tag--cyan">Bcrypt / Argon2</span>
    <span class="card-tag card-tag--cyan">TLS</span>
</div>

<h2>🎯 Contexte</h2>

<p>Étude de cas sur une plateforme de streaming à construire, traitée sous deux angles à la fois : la conduite du projet et la sécurité de l'application produite. L'exercice demandait de livrer un plan de charge tenable et une architecture de sécurité justifiée, pas seulement une liste de bonnes pratiques.</p>

<h2>⚙️ Volet pilotage</h2>

<ul>
    <li><strong>Backlog et sprints.</strong> Découpage des besoins en récits utilisateur estimés, priorisation par valeur métier et organisation en sprints avec un tableau Jira pour le suivi quotidien.</li>
    <li><strong>Planification.</strong> Construction du diagramme de Gantt avec les dépendances entre lots, le chemin critique et les jalons de recette, ce qui a permis de repérer en amont les tâches où un retard décale toute la suite.</li>
    <li><strong>Suivi.</strong> Définition des rituels, des critères de fin pour chaque récit et des indicateurs d'avancement présentés en revue de sprint.</li>
</ul>

<h2>🔐 Volet sécurité applicative</h2>

<ul>
    <li><strong>Authentification.</strong> Double facteur à l'ouverture de session, jetons JWT de courte durée associés à des jetons de renouvellement, et gestion granulaire des rôles côté serveur plutôt que côté interface.</li>
    <li><strong>Stockage des secrets.</strong> Hachage des mots de passe avec Bcrypt puis Argon2, avec salage et paramétrage du coût en fonction de la charge attendue.</li>
    <li><strong>Audit OWASP.</strong> Revue des dix risques les plus courants appliqués au périmètre du projet, avec pour chacun le scénario d'exploitation et la contre-mesure retenue. Les injections, les défauts de contrôle d'accès et l'exposition de données sensibles ont concentré l'essentiel des corrections.</li>
    <li><strong>Chiffrement des flux.</strong> Standards TLS imposés, suites cryptographiques obsolètes retirées et redirection systématique du trafic en clair.</li>
</ul>

<h2>📄 Livrables</h2>

<div class="card-result">📎 <a href="{{ '/docs/agile-presentation-finale.pdf' | relative_url }}">Présentation finale du projet (PDF)</a></div>
<div class="card-result">📎 <a href="{{ '/docs/agile-document-analyse.pdf' | relative_url }}">Document d'analyse (PDF)</a></div>
<div class="card-result">📎 <a href="{{ '/docs/agile-gantt-netflix.pdf' | relative_url }}">Planification Gantt de la plateforme (PDF)</a></div>
<div class="card-result">📎 <a href="{{ '/docs/agile-gantt-pme.pdf' | relative_url }}">Planification Gantt, architecture d'une PME (PDF)</a></div>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
