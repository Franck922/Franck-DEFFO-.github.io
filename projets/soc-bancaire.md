---
layout: default
title: SOC & Supervision Bancaire
---

<div class="project-detail">

<span class="card-label card-label--cyan">Supervision & Détection · Février 2026</span>

<h1>🛡️ SOC & Supervision : Infrastructure Bancaire Critique</h1>

<div style="margin-bottom: 2rem;">
  <a href="https://github.com/Franck922/Security-Operations-Center-Wazuh-Grafana" target="_blank" style="display: inline-flex; align-items: center; gap: 0.5rem; background: #1e293b; color: white; padding: 0.5rem 1rem; border-radius: 8px; text-decoration: none; font-weight: 600;">
    <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    Voir le code source sur GitHub
  </a>
</div>

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
