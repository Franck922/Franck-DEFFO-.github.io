---
layout: default
title: API REST de gestion de voyages en Java Spring Boot
description: API REST en Java et Spring Boot : architecture en couches, Spring Data JPA, documentation Swagger, tests JUnit et collections Postman.
---

<div class="project-detail">

<span class="card-label">Développement back-end · 2025</span>

<h1>☕ API REST de gestion de voyages en Java Spring Boot</h1>

<div class="card-tags">
    <span class="card-tag">Java</span>
    <span class="card-tag">Spring Boot</span>
    <span class="card-tag">Spring Data JPA</span>
    <span class="card-tag">Hibernate</span>
    <span class="card-tag">MySQL</span>
    <span class="card-tag">Swagger / OpenAPI</span>
    <span class="card-tag">JUnit</span>
    <span class="card-tag">Postman</span>
    <span class="card-tag">Maven</span>
</div>

<h2>🎯 Contexte</h2>

<p>Reprise du même domaine métier que la plateforme Laravel, cette fois sur la pile Java. L'intérêt de l'exercice était de comparer deux écosystèmes sur un besoin identique et de travailler des sujets que Laravel masque en partie, en particulier la gestion explicite des transactions et le contrôle des requêtes générées par l'ORM.</p>

<h2>⚙️ Architecture</h2>

<ul>
    <li><strong>Découpage en couches.</strong> Contrôleurs pour l'exposition HTTP, services pour les règles métier, repositories pour l'accès aux données. Les objets de transfert isolent les entités persistées de ce qui circule sur le réseau, ce qui évite d'exposer le schéma de base aux consommateurs.</li>
    <li><strong>Persistance.</strong> Entités JPA et relations gérées par Hibernate, requêtes dérivées et requêtes personnalisées quand la dérivation ne suffit plus.</li>
    <li><strong>Transactions.</strong> Délimitation des opérations qui doivent réussir ou échouer ensemble, avec le comportement de retour arrière attendu en cas d'exception.</li>
    <li><strong>Gestion des erreurs.</strong> Traitement centralisé par gestionnaire d'exceptions, avec un format de réponse uniforme et des codes HTTP conformes à la nature de l'erreur.</li>
</ul>

<h2>🧪 Documentation et tests</h2>

<ul>
    <li><strong>Swagger.</strong> Documentation générée depuis le code, ce qui garde la référence alignée sur l'implémentation et permet d'essayer les points d'entrée directement depuis le navigateur.</li>
    <li><strong>JUnit.</strong> Tests unitaires sur la couche service, avec simulation des repositories pour isoler la logique métier de la base.</li>
    <li><strong>Postman.</strong> Collections réutilisables couvrant les parcours principaux, variables d'environnement pour basculer entre local et distant.</li>
    <li><strong>Performance.</strong> Analyse des requêtes émises par Hibernate et correction des chargements en cascade non maîtrisés, qui multipliaient inutilement les allers-retours vers la base.</li>
</ul>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
