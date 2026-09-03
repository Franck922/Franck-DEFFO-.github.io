---
layout: default
title: Analyse de Menaces MITRE ATT&CK
---

<div class="project-detail">

<span class="card-label card-label--cyan">Gouvernance & Cyber Threat Intelligence · Janvier 2026</span>

<h1>🛡️ Analyse de Menaces : Modélisation via MITRE ATT&CK & D3FEND</h1>

<div class="card-tags">
    <span class="card-tag--cyan card-tag">MITRE ATT&CK</span>
    <span class="card-tag--cyan card-tag">MITRE D3FEND</span>
    <span class="card-tag--cyan card-tag">SCADA (ICS)</span>
    <span class="card-tag--cyan card-tag">CTI</span>
    <span class="card-tag--cyan card-tag">ISO 27005</span>
</div>

<h2>🎯 Contexte et Objectifs</h2>

<p>Comprendre "comment" un attaquant opère est le prérequis indispensable pour défendre un système efficacement. Ce projet de recherche appliquée consistait à analyser des attaques réelles ciblant des secteurs critiques (Systèmes industriels SCADA et domaine hôtelier), et à les modéliser en utilisant les standards de l'industrie pour la Cyber Threat Intelligence (CTI).</p>

<h2>⚙️ Méthodologie et Actions Menées (Méthode STAR)</h2>

<ul>
    <li><strong>Situation :</strong> Face à des scénarios d'attaques complexes (ex: APT ciblant un réseau électrique industriel), il fallait décomposer l'attaque pour identifier précisément les failles exploitées et proposer des contre-mesures adaptées.</li>
    <li><strong>Tâche :</strong> Maper (cartographier) les comportements offensifs sur la matrice MITRE ATT&CK, évaluer l'impact via la méthode ISO 27005, et concevoir une architecture défensive avec MITRE D3FEND.</li>
    <li><strong>Action (Modélisation Offensive - ATT&CK) :</strong> J'ai décomposé le cycle de vie de l'attaque en Tactics, Techniques, and Procedures (TTPs). J'ai retracé le parcours de l'attaquant : depuis l'accès initial (Phishing, exploitation d'équipement frontal) jusqu'à l'impact (manipulation de systèmes de contrôle SCADA, exfiltration), en passant par l'élévation de privilèges.</li>
    <li><strong>Action (Évaluation des Risques - ISO 27005) :</strong> J'ai quantifié les conséquences de ces TTPs sur les processus métiers (perte de disponibilité de l'usine, fuite de données clients de l'hôtel) pour prioriser les chantiers de sécurisation.</li>
    <li><strong>Action (Modélisation Défensive - D3FEND) :</strong> Face à chaque technique identifiée, j'ai sélectionné les contre-mesures techniques appropriées dans la matrice D3FEND (ex: analyse comportementale des processus, segmentation réseau OT/IT, durcissement des authentifications).</li>
</ul>

<h2>📈 Résultats et Impact</h2>

<div class="card-result">✅ Livrable : <strong>Kill Chain complète</strong> documentée pour des scénarios ICS/SCADA.</div>
<div class="card-result">✅ Livrable : <strong>Matrice d'atténuation</strong> corrélant directement l'attaque (ATT&CK) à la défense (D3FEND).</div>

<p><strong>Conclusion :</strong> Ce travail d'analyse m'a doté d'une forte capacité de modélisation des menaces (Threat Modeling). Je sais désormais exploiter des bases de connaissances CTI pour orienter l'architecture de sécurité, transformer la donnée de renseignement en actions techniques concrètes, et aligner ces choix avec la stratégie globale des risques (ISO 27005).</p>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
