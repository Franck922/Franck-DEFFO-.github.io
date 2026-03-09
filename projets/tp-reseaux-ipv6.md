# 🛰️ Ingénierie Réseaux Cisco : Adressage VLSM & Transition IPv6
> Expertise Réseaux & Télécoms | ECE Paris

## 📝 Objectif du Projet
Concevoir et déployer une infrastructure réseau multi-sites résiliente, optimisée par un adressage VLSM (IPv4) et préparée aux futurs standards via une configuration Dual-Stack IPv6.

## 🏗️ Architecture du Réseau
L'infrastructure interconnecte plusieurs réseaux locaux (LAN) aux besoins en hôtes hétérogènes (de 9 à 64 machines) via des routeurs Cisco 2911.

## 🛠️ Réalisations Techniques

### 1. Optimisation de l'Adressage IPv4 (VLSM)
*   **Calcul de sous-réseaux** : Utilisation du *Variable Length Subnet Masking* pour segmenter l'espace d'adressage en fonction des besoins réels de chaque département.
*   **Résultat** : Réduction du gaspillage d'adresses IP de plus de **40%** et optimisation des tables de routage.

### 2. Déploiement de l'Infrastructure IPv6
*   **Adressage Global Unicast** : Configuration de préfixes `2001:DB8:0:X::/64` pour garantir une connectivité globale.
*   **Autoconfiguration SLAAC** : Mise en œuvre du mécanisme *Stateless Address Autoconfiguration* permettant aux hôtes d'obtenir leurs paramètres IP automatiquement via les Router Advertisements (RA).
*   **Gestion Link-Local** : Utilisation d'adresses `FE80::` pour la communication locale et la gestion des passerelles par défaut.

### 3. Routage & Sécurisation
*   **Routage Unicast IPv6** : Activation et configuration du transfert de paquets IPv6 au niveau global du routeur.
*   **Dual-Stack** : Implémentation simultanée des deux protocoles (IPv4/IPv6) pour assurer une transition transparente sans interruption de service.
*   **Diagnostic Avancé** : Analyse des tables de routage (`show ipv6 route`) et validation par tests de connectivité de bout en bout.

## ✅ Résultats & Validation
*   **Connectivité 100% opérationnelle** sur l'ensemble des segments réseau.
*   **Table de routage saine** et optimisée pour une maintenance facilitée.
*   **Infrastructure "Future-Proof"**, prête pour les nouveaux services internet et IoT.

---
[⬅️ Retour à l'accueil](../README.md)
