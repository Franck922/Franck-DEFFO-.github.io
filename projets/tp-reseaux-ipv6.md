---
layout: default
title: Adressage VLSM et transition IPv6
description: Conception d'une infrastructure multi-sites Cisco avec adressage VLSM en IPv4 et déploiement d'une pile double IPv6.
---

<div class="project-detail">

<span class="card-label card-label--purple">Réseaux et télécoms · ECE Paris</span>

<h1>🛰️ Adressage VLSM et transition IPv6</h1>

<div class="card-tags">
    <span class="card-tag card-tag--purple">Cisco 2911</span>
    <span class="card-tag card-tag--purple">VLSM</span>
    <span class="card-tag card-tag--purple">IPv6</span>
    <span class="card-tag card-tag--purple">SLAAC</span>
    <span class="card-tag card-tag--purple">Dual-Stack</span>
</div>

<h2>📝 Objectif</h2>

<p>Concevoir une infrastructure multi-sites résiliente, optimisée par un adressage VLSM en IPv4 et préparée aux standards actuels grâce à une configuration en pile double IPv6.</p>

<h2>🏗️ Architecture du réseau</h2>

<p><img src="{{ '/topologie-ipv6.png' | relative_url }}" alt="Topologie réseau IPv6" /></p>

<p>Infrastructure interconnectant trois réseaux locaux distincts via un routeur Cisco 2911, avec segmentation par zones.</p>

<h2>🛠️ Réalisations techniques</h2>

<h3>Ingénierie de l'adressage</h3>

<ul>
    <li><strong>Optimisation IPv4.</strong> Calcul de sous-réseaux à masques variables pour répondre au besoin réel de chaque réseau local, de 9 à 64 hôtes, sans gaspiller de plages.</li>
    <li><strong>Déploiement IPv6.</strong> Adressage Global Unicast et configuration du mécanisme SLAAC pour l'autoconfiguration des postes clients.</li>
</ul>

<h3>Routage et diagnostic</h3>

<ul>
    <li><strong>Routage unicast.</strong> Activation du transfert de paquets IPv6 et configuration des passerelles par défaut.</li>
    <li><strong>Vérification.</strong> Analyse des tables de routage pour garantir l'étanchéité entre segments et la bonne circulation des flux.</li>
</ul>

<h2>✅ Validation</h2>

<p>La conformité de l'infrastructure est confirmée par des tests de connectivité de bout en bout entre tous les segments du réseau.</p>

<p><img src="{{ '/ping-ipv6.png' | relative_url }}" alt="Test ping IPv6" /></p>

<p>Tests de ping réussis en IPv6, validant la communication entre le poste client et les réseaux distants.</p>

<h2>📄 Documentation</h2>

<div class="card-result">📎 <a href="{{ '/TP4%20Ipv4-Ipv6-DFSM.pdf' | relative_url }}">Rapport technique complet (PDF)</a></div>
<div class="card-result">📎 <a href="{{ '/RAPPORT%20TP%20MINI%20PROJET.pdf' | relative_url }}">Rapport du mini projet réseau (PDF)</a></div>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
