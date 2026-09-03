---
layout: default
title: POC Cyber Limited
---

<div class="project-detail">

<span class="card-label">Durcissement & Architecture · 2025</span>

<h1>🛡️ POC Cyber Limited : Création & Durcissement d'une Infrastructure</h1>

<div class="card-tags">
    <span class="card-tag">pfSense</span>
    <span class="card-tag">Snort (IDS)</span>
    <span class="card-tag">Fail2ban</span>
    <span class="card-tag">Windows Server</span>
    <span class="card-tag">Linux / GPO</span>
</div>

<h2>🎯 Contexte et Objectifs</h2>

<p>Dans le cadre de l'entreprise fictive "Cyber Limited", la mission était de partir d'une feuille blanche pour concevoir, déployer et surtout <strong>durcir (harden)</strong> l'ensemble de l'infrastructure réseau et système. Le but n'était pas seulement de faire communiquer des machines, mais de garantir un niveau de sécurité "Defense in Depth" (Défense en profondeur).</p>

<h2>⚙️ Méthodologie et Actions Menées (Méthode STAR)</h2>

<ul>
    <li><strong>Situation :</strong> L'entreprise nécessitait une segmentation réseau stricte (LAN utilisateurs, DMZ pour les services exposés) et un durcissement des systèmes d'exploitation pour prévenir les mouvements latéraux en cas d'intrusion.</li>
    <li><strong>Tâche :</strong> Concevoir la topologie, configurer le pare-feu de bordure, implémenter la détection d'intrusion réseau (NIDS) et appliquer les politiques de sécurité sur les serveurs Windows et Linux.</li>
    <li><strong>Action (Architecture Réseau & Pare-feu) :</strong> J'ai déployé <strong>pfSense</strong> comme cœur de réseau. J'ai créé les VLANs nécessaires et écrit des règles de filtrage strictes (Default Deny) limitant les flux inter-zones au strict nécessaire.</li>
    <li><strong>Action (Détection d'Intrusion) :</strong> J'ai configuré <strong>Snort</strong> sur l'interface WAN de pfSense pour détecter les signatures d'attaques connues, et j'ai installé <strong>Fail2ban</strong> sur les serveurs exposés pour bannir automatiquement les adresses IP tentant des attaques par force brute.</li>
    <li><strong>Action (Durcissement Système) :</strong> Sur la partie Windows, j'ai implémenté des <strong>GPO (Group Policy Objects)</strong> contraignantes (complexité des mots de passe, désactivation des protocoles obsolètes comme SMBv1, restrictions LAPS). Sur Linux, j'ai configuré le pare-feu local (iptables/ufw) et durci la configuration SSH.</li>
</ul>

<h2>📈 Résultats et Impact</h2>

<div class="card-result">✅ <strong>Segmentation validée :</strong> Réussite des tests d'étanchéité entre la DMZ et le LAN interne.</div>
<div class="card-result">✅ <strong>Audits de sécurité passés :</strong> La politique de mot de passe et le durcissement réseau ont bloqué efficacement les tests d'intrusion basiques simulés.</div>

<p><strong>Conclusion :</strong> Ce Proof of Concept (POC) démontre ma maîtrise concrète de l'administration système et réseau orientée sécurité. Je suis capable d'appliquer les principes du moindre privilège et de la défense en profondeur sur des environnements hétérogènes (Windows/Linux).</p>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
