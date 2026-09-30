---
layout: default
title: Jeu de plateforme 2D sous Unity
description: Jeu de plateforme développé en C# avec Unity : déplacement du personnage, intelligence des ennemis, système de vie, collectables et interface.
---

<div class="project-detail">

<span class="card-label">Développement · Temps réel · 2024 à 2025</span>

<h1>🎮 Jeu de plateforme 2D sous Unity</h1>

<div class="card-tags">
    <span class="card-tag">Unity</span>
    <span class="card-tag">C#</span>
    <span class="card-tag">Physique 2D</span>
    <span class="card-tag">Machine à états</span>
    <span class="card-tag">TextMesh Pro</span>
</div>

<h2>🎯 Contexte</h2>

<p>Projet personnel mené pour comprendre ce qui se passe entre deux images d'un jeu : la boucle de mise à jour, la détection de collisions et la gestion d'état des entités. Le moteur Unity sert de support, mais toute la logique de jeu a été écrite en C# depuis une page blanche, sans partir d'un modèle tout fait.</p>

<h2>⚙️ Ce que contient le projet</h2>

<ul>
    <li><strong>Contrôle du personnage.</strong> Déplacement latéral et saut avec gestion de la gravité, détection du contact au sol et animation synchronisée sur l'état du joueur.</li>
    <li><strong>Ennemis.</strong> Deux comportements distincts, une patrouille sur trajet fixe avec demi-tour aux limites, et une poursuite qui s'enclenche quand le joueur entre dans le rayon de détection. Le contact inflige des dégâts avec une courte période d'invulnérabilité pour éviter la perte de vie en rafale.</li>
    <li><strong>Points de vie et interface.</strong> Système de vie du joueur relié à l'affichage, retour visuel à chaque perte et condition de fin de partie.</li>
    <li><strong>Collectables et score.</strong> Ramassage d'objets par détection de déclencheur, mise à jour du compteur et son associé.</li>
    <li><strong>Structure générale.</strong> Un gestionnaire de partie centralise l'état, un gestionnaire audio prend en charge la musique et les effets, et un menu principal permet de lancer ou de quitter la partie.</li>
</ul>

<h2>📈 Ce que le projet m'a apporté</h2>

<p>Le jeu impose une discipline que les applications de gestion n'imposent pas : tout doit tenir dans le temps d'une image, et un objet mal détruit finit par se voir à l'écran. Travailler la séparation entre l'état, le rendu et l'entrée utilisateur m'a servi ensuite sur des applications web, où le même découpage rend le code bien plus facile à corriger.</p>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
