---
layout: default
title: Plateforme de gestion de voyages, Laravel et Vue.js
description: Application web complète en Laravel et Vue.js : authentification, gestion des rôles, réservations, API REST et interface d'administration.
---

<div class="project-detail">

<span class="card-label">Développement web · 2024 à 2025</span>

<h1>✈️ Plateforme de gestion de voyages en Laravel et Vue.js</h1>

<div class="card-tags">
    <span class="card-tag">PHP</span>
    <span class="card-tag">Laravel</span>
    <span class="card-tag">Vue.js</span>
    <span class="card-tag">MySQL</span>
    <span class="card-tag">Eloquent ORM</span>
    <span class="card-tag">API REST</span>
    <span class="card-tag">Tailwind CSS</span>
</div>

<h2>🎯 Contexte</h2>

<p>Application de gestion de voyages construite en deux parties séparées, une interface cliente qui consomme une API et un back-office pour l'administration. Ce découpage a été choisi pour que le front puisse évoluer sans toucher aux règles métier, et pour exposer les mêmes données à un éventuel client mobile.</p>

<h2>⚙️ Côté serveur (Laravel)</h2>

<ul>
    <li><strong>Modélisation.</strong> Schéma relationnel sous MySQL avec migrations versionnées, relations Eloquent entre voyages, réservations, clients et destinations, et jeux de données de démonstration pour reproduire l'environnement en une commande.</li>
    <li><strong>Authentification et rôles.</strong> Inscription, connexion et gestion de session, avec des droits distincts entre client et administrateur. Les contrôles sont appliqués côté serveur par des intergiciels, l'interface se contentant de masquer ce qui n'est pas accessible.</li>
    <li><strong>API REST.</strong> Ressources exposées en JSON, validation des requêtes entrantes, codes de réponse cohérents et traitement centralisé des erreurs.</li>
    <li><strong>Sécurité.</strong> Protection contre la falsification de requête, requêtes préparées via l'ORM pour écarter les injections SQL, échappement des sorties et hachage des mots de passe.</li>
</ul>

<h2>💻 Côté client (Vue.js)</h2>

<ul>
    <li>Interface en composants réutilisables, avec navigation entre les vues et état partagé entre les écrans.</li>
    <li>Appels asynchrones vers l'API, états de chargement et affichage des messages d'erreur renvoyés par le serveur.</li>
    <li>Formulaires de recherche et de réservation avec validation avant envoi, puis mise en forme responsive.</li>
</ul>

<h2>📦 Dépôts</h2>

<div class="card-result">💻 <a href="https://github.com/Franck922/projet_backend" target="_blank" rel="noopener">Dépôt du back-end Laravel</a></div>
<div class="card-result">💻 <a href="https://github.com/Franck922/projet_frontend" target="_blank" rel="noopener">Dépôt du front-end</a></div>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
