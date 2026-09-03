---
layout: default
title: SOC & Supervision Bancaire
---

<div class="project-detail">

<span class="card-label card-label--cyan">Supervision & Détection · Février 2026</span>

<h1>🛡️ SOC & Supervision : Infrastructure Bancaire Critique</h1>

<div class="card-tags">
    <span class="card-tag--cyan card-tag">SIEM Wazuh</span>
    <span class="card-tag--cyan card-tag">FIM</span>
    <span class="card-tag--cyan card-tag">Zabbix</span>
    <span class="card-tag--cyan card-tag">Grafana</span>
    <span class="card-tag--cyan card-tag">Linux</span>
</div>

<h2>🎯 Contexte et Objectifs</h2>

<p>Le secteur bancaire est l'un des plus régulés et ciblés par les cyberattaques. La compromission d'une donnée financière ou l'indisponibilité d'un service critique (déni de service) a des conséquences désastreuses. L'objectif de ce projet était de construire un <strong>Security Operations Center (SOC) miniature mais complet</strong>, capable de monitorer, détecter et alerter sur des comportements anormaux au sein d'une infrastructure critique simulée.</p>

<h2>⚙️ Méthodologie et Actions Menées (Méthode STAR)</h2>

<ul>
    <li><strong>Situation :</strong> L'infrastructure bancaire simulée (composée de 5 machines virtuelles Linux : serveurs web, base de données, rebond) était aveugle aux attaques réseau et aux modifications système non autorisées.</li>
    <li><strong>Tâche :</strong> Concevoir et déployer une solution de supervision globale (disponibilité et sécurité) pour centraliser les logs, détecter les intrusions et visualiser l'état de santé du SI en temps réel.</li>
    <li><strong>Action (Supervision Sécurité) :</strong> J'ai déployé le SIEM open-source <strong>Wazuh</strong> (manager et agents). J'ai configuré l'ingestion des logs système (syslog, auth.log) et activé le module <strong>FIM (File Integrity Monitoring)</strong> pour alerter immédiatement sur toute modification des fichiers de configuration critiques (ex: <code>/etc/shadow</code>, <code>/etc/ssh/sshd_config</code>).</li>
    <li><strong>Action (Détection d'Attaques) :</strong> J'ai simulé des attaques réalistes (Brute Force SSH, requêtes HTTP malveillantes type injection SQL) et j'ai écrit/ajusté des règles de détection Wazuh pour générer des alertes de haute sévérité.</li>
    <li><strong>Action (Supervision Disponibilité & Dashboarding) :</strong> En parallèle de la sécurité, j'ai mis en place <strong>Zabbix</strong> pour le monitoring matériel (CPU, RAM, Disque, temps de réponse réseau) et j'ai connecté <strong>Grafana</strong> pour créer des tableaux de bord (dashboards) unifiés et esthétiques à destination de l'équipe d'analystes.</li>
</ul>

<h2>📈 Résultats et Impact</h2>

<div class="card-result">✅ <strong>Détection en temps réel :</strong> Les attaques par force brute et les modifications de fichiers critiques sont remontées en moins de 5 secondes sur la console Wazuh.</div>
<div class="card-result">✅ <strong>Visibilité totale :</strong> Le tableau de bord Grafana offre une vue "single pane of glass" sur la santé et la sécurité des 5 VMs.</div>

<p><strong>Conclusion :</strong> Ce projet prouve ma capacité à intégrer et configurer des outils open-source standards de l'industrie (Wazuh, Zabbix, Grafana) pour bâtir une chaîne de défense robuste. J'ai compris l'importance de la corrélation des événements et de la réduction du bruit (faux positifs) pour ne pas noyer les analystes SOC sous les alertes.</p>

<a href="{{ '/' | relative_url }}" class="back-link">← Retour au portfolio</a>

</div>
