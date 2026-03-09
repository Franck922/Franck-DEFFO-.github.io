# 🛡️ Analyse Offensive & Stratégies de Défense (MITRE ATT&CK & D3FEND)
> **Étude de Cas Cybersécurité Multi-Secteurs | Keyce Academy**

---
### 📄 [Consulter le Rapport d'Analyse Complet (PDF)](../Rapport-final-groupe-1-Franck-DEFFO.pdf)
---

## 📝 Objectif de l'Étude
Ce projet visait à modéliser le mode opératoire d'attaquants à travers deux scénarios réalistes. L'objectif était de décomposer chaque phase de l'attaque (Offensif) pour en déduire les contre-mesures les plus efficaces (Défensif).

---

## 🏨 Scénario 1 : Compromission d'un Système Hôtelier
**Problématique** : Exfiltration de données clients via des failles web.

### 🔍 Analyse de la Kill Chain
1.  **Accès Initial** : Exploitation d'une faille d'upload non sécurisée sur le serveur web de réservation.
2.  **Exécution** : Téléversement et exécution d'un **Web Shell PHP** pour obtenir une interface de commande à distance.
3.  **Escalade de Privilèges** : Utilisation d'un exploit Kernel pour obtenir les droits **Root**.
4.  **Exfiltration** : Collecte et transfert des bases de données SQL vers un serveur externe.

### 🛡️ Réponses Défensives (D3FEND)
*   **Validation des entrées** : Filtrage strict des types de fichiers autorisés à l'upload.
*   **Patch Management** : Mise à jour du noyau système pour corriger les vulnérabilités locales.

---

## ⚡ Scénario 2 : Ransomware sur Réseau Industriel (SCADA)
**Problématique** : Attaque ciblée sur une infrastructure de distribution d'énergie.

### 🔍 Analyse du Mode Opératoire
1.  **Infiltration** : Campagne de **Spear Phishing** ciblant un technicien avec une pièce jointe malveillante.
2.  **Mouvement Latéral** : Re-use d'identifiants et exploitation de failles de partage réseau (SMB) pour atteindre les serveurs de contrôle SCADA.
3.  **Impact** : Chiffrement des systèmes de gestion et demande de rançon (Ransomware).

### 🛡️ Stratégies de Résilience
*   **Segmentation IT/OT** : Isolation du réseau industriel pour empêcher la propagation depuis le réseau bureautique.
*   **Credential Hardening** : Mise en œuvre du MFA (Authentification multi-facteurs).
*   **Sauvegardes Hors-Ligne** : Stratégie de backup immuable pour garantir la reprise d'activité.

## ✅ Résultats & Apports
Ce projet démontre ma capacité à :
*   Utiliser les référentiels mondiaux (**MITRE ATT&CK**) pour cartographier une menace.
*   Proposer un **Plan d'Action de Sécurité** structuré et hiérarchisé.
*   Comprendre les enjeux de cybersécurité spécifiques au monde industriel (**OT**).

---
[⬅️ Retour à l'accueil](../README.md)
