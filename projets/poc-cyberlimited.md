---
layout: default
title: POC Cyber Limited
---

<div class="project-detail">

<span class="card-label">Durcissement & Architecture · 2025</span>

<h1>🛡️ POC Cyber Limited : Création & Durcissement d'une Infrastructure</h1>

<div style="margin-bottom: 2rem;">
  <a href="https://github.com/Franck922/POC-CyberLimited-Security-Hardening" target="_blank" style="display: inline-flex; align-items: center; gap: 0.5rem; background: #1e293b; color: white; padding: 0.5rem 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
    <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    Voir le code source sur GitHub
  </a>
</div>

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
