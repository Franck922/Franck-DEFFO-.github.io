---
layout: default
title: Réseau multi-sites et tunnel IPsec
description: Segmentation VLAN, routage OSPF, NAT et tunnel IPsec site à site sur équipements Cisco, avec durcissement de l'administration.
---

<div class="project-detail">

<span class="card-label card-label--purple">Réseaux · NOV 2025 à JANV 2026</span>

<h1>🌐 Réseau multi-sites et tunnel IPsec</h1>

<div class="card-tags">
    <span class="card-tag card-tag--purple">Cisco IOS</span>
    <span class="card-tag card-tag--purple">VLAN · 802.1Q · VTP</span>
    <span class="card-tag card-tag--purple">Spanning Tree</span>
    <span class="card-tag card-tag--purple">OSPF</span>
    <span class="card-tag card-tag--purple">NAT / PAT</span>
    <span class="card-tag card-tag--purple">IPsec</span>
    <span class="card-tag card-tag--purple">IPv6</span>
    <span class="card-tag card-tag--purple">SSHv2</span>
</div>

<h2>🎯 Contexte</h2>

<p>Une entreprise répartie sur plusieurs sites distants doit faire circuler son trafic interne sans l'exposer sur Internet, tout en cloisonnant ses services les uns des autres. Cette série de travaux pratiques couvre l'architecture complète, de la couche 2 jusqu'au chiffrement du transport entre sites.</p>

<h2>⚙️ Travaux menés</h2>

<ul>
    <li><strong>Segmentation de niveau 2.</strong> Découpage en VLAN par service, liaisons trunk en 802.1Q entre commutateurs et propagation de la base VLAN par VTP. Le Spanning Tree a été réglé pour placer la racine sur le commutateur de distribution plutôt que de laisser l'élection au hasard des adresses MAC.</li>
    <li><strong>Routage dynamique.</strong> Mise en place d'OSPF sur plusieurs aires, avec vérification des tables de voisinage et des états d'adjacence, puis analyse du comportement de convergence après coupure d'un lien.</li>
    <li><strong>Adressage et transition IPv6.</strong> Plan d'adressage en VLSM pour limiter le gaspillage, puis mise en œuvre d'une pile double IPv4 et IPv6 avec le routage associé.</li>
    <li><strong>Sortie Internet.</strong> Traduction d'adresses en NAT statique pour les serveurs publiés et en PAT pour les postes clients.</li>
    <li><strong>Tunnel site à site.</strong> Établissement d'un tunnel IPsec entre deux sites, chiffrement AES et intégrité par SHA-HMAC, avec négociation IKE et vérification des associations de sécurité.</li>
    <li><strong>Durcissement de l'administration.</strong> Remplacement de Telnet par SSHv2, mots de passe chiffrés, bannières légales et fermeture des lignes d'accès non utilisées.</li>
</ul>

<h2>🔍 Validation</h2>

<p>Chaque configuration a été vérifiée par capture Wireshark et par les commandes de diagnostic Cisco. Sur le tunnel IPsec, la capture montre le trafic en clair avant chiffrement sur le réseau local et encapsulé en ESP sur le lien intersites, ce qui prouve que la protection s'applique bien au bon endroit.</p>

<h2>📄 Rapports techniques</h2>

<div class="card-result">📎 <a href="{{ '/docs/rapport-ospf-tp6.pdf' | relative_url }}">Routage dynamique OSPF (PDF)</a></div>
<div class="card-result">📎 <a href="{{ '/docs/rapport-vlan-stp-lab2.pdf' | relative_url }}">Segmentation VLAN et Spanning Tree (PDF)</a></div>
<div class="card-result">📎 <a href="{{ '/docs/rapport-ipv6-lab3.pdf' | relative_url }}">Mise en œuvre IPv6 (PDF)</a></div>
<div class="card-result">📎 <a href="{{ '/Projets/tp-reseaux-ipv6' | relative_url }}">Adressage VLSM et transition IPv6, page détaillée</a></div>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
