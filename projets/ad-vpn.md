---
layout: default
title: TechSecure - AD & VPN PKI
---

<div class="project-detail">

<span class="card-label card-label--purple">Active Directory & Réseau · 2025</span>

<h1>🛡️ TechSecure : Infrastructure Active Directory & VPN PKI</h1>

<div class="card-tags">
    <span class="card-tag--purple card-tag">Windows Server 2019</span>
    <span class="card-tag--purple card-tag">Active Directory (AD DS)</span>
    <span class="card-tag--purple card-tag">GPO / DNS</span>
    <span class="card-tag--purple card-tag">OpenVPN</span>
    <span class="card-tag--purple card-tag">PKI (Easy-RSA)</span>
</div>

<h2>🎯 Contexte et Objectifs</h2>

<p>Pour répondre aux besoins de mobilité et de télétravail de l'entreprise "TechSecure", ce projet visait à concevoir le cœur du réseau d'entreprise (gestion des identités) et à y greffer un accès distant hautement sécurisé, reposant sur une authentification forte par certificats.</p>

<h2>⚙️ Méthodologie et Actions Menées (Méthode STAR)</h2>

<ul>
    <li><strong>Situation :</strong> L'entreprise nécessitait un annuaire centralisé pour gérer ses employés et ses ressources, ainsi qu'une solution permettant aux travailleurs distants d'accéder aux serveurs internes sans exposer l'infrastructure sur Internet.</li>
    <li><strong>Tâche :</strong> Déployer et configurer un domaine Active Directory complet, puis implémenter un tunnel VPN sécurisé basé sur une PKI (Public Key Infrastructure).</li>
    <li><strong>Action (Gouvernance des Identités - AD DS) :</strong> J'ai installé et promu un contrôleur de domaine sous <strong>Windows Server 2019</strong>. J'ai structuré l'annuaire (OU, groupes de sécurité) en respectant les rôles métiers. J'ai également configuré les services d'infrastructure vitaux (serveur <strong>DNS</strong>).</li>
    <li><strong>Action (Stratégies de Sécurité - GPO) :</strong> J'ai déployé des <strong>Objets de Stratégie de Groupe (GPO)</strong> pour standardiser la sécurité du parc : blocage des périphériques USB non autorisés, mappage automatique des lecteurs réseaux chiffrés, et déploiement de scripts de démarrage.</li>
    <li><strong>Action (Accès Distant - OpenVPN & PKI) :</strong> J'ai déployé un serveur <strong>OpenVPN</strong> sous Linux. Au lieu d'une simple authentification par mot de passe (vulnérable), j'ai monté une autorité de certification (<strong>Easy-RSA</strong>) pour générer des certificats clients uniques. Le VPN ne s'établit que si le client possède la clé privée correspondante.</li>
</ul>

<h2>📈 Résultats et Impact</h2>

<div class="card-result">✅ <strong>Centralisation réussie :</strong> Authentification unique (SSO) pour l'ensemble des utilisateurs sur le domaine.</div>
<div class="card-result">✅ <strong>Télétravail sécurisé :</strong> Tunnel VPN robuste empêchant toute attaque par interception (Man-in-the-Middle) grâce au chiffrement TLS et à la vérification des certificats.</div>

<p><strong>Conclusion :</strong> Ce projet valide ma compréhension des socles d'infrastructure d'entreprise (Active Directory) qui restent omniprésents, et ma capacité à y intégrer des solutions de sécurité réseau modernes et open-source pour répondre aux enjeux de mobilité.</p>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
