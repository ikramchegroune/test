# Readme File: Edge Router and ISPs Overview

---

## Overview de l'Architecture du Routeur (Edge Router) et des Fournisseurs de Services Internet (ISPs)

Ce document fournit un aperçu de l'architecture du routeur de bordure (Edge Router) et des fournisseurs de services Internet (ISPs) qui sont des composants essentiels de l'infrastructure réseau d'une entreprise. L'Edge Router, nommé vIOS-EDGE-I, assure la connectivité entre le réseau de l'entreprise et Internet via deux ISPs. Les ISPs, ISP1 et ISP2, fournissent les connexions Internet au routeur de bordure (Edge Router). Cette architecture permet à l'entreprise d'accéder à Internet de manière sécurisée et fiable.
### Contenu :

1. **Introduction**
2. **Composants de l'architecture**
3. **Résumé de la configuration**
4. **Dépannage et surveillance**
5. **Mesures de sécurité**
6. **Conclusion**

---
## 1. Introduction :

L'architecture du routeur Edge et des ISPs joue un rôle important dans l'infrastructure réseau d'une entreprise. Elle permet à l'entreprise d'établir des connexions sécurisées et fiables avec Internet, essentielles pour ses opérations quotidiennes.

## 2. Composants de l'architecture :

Cette architecture comprend les composants suivants :

- **Edge Router (vIOS-EDGE-I) :**  Agit comme la passerelle de sécurité principale entre le réseau interne et l'internet. Il filtre le trafic entrant et sortant en fonction de règles et de politiques prédéfinies.

- **Fournisseurs de Services Internet (ISPs) :**  Fournissent les connexions Internet pour l'architecture en passent par  Edge router. Les ISPs sont responsables de l'acheminement du trafic Internet de l'entreprise vers Internet et vice versa.

## 3. Résumé de la configuration :

La configuration détaillée du routeur de bordure (vIOS-EDGE-I) et des ISPs (ISP1 et ISP2) est décrite dans des fichiers séparés. Cette configuration comprend :

- **Configuration du routeur de bordure (vIOS-EDGE-I) :**  Définit la configuration initiale, les informations d'identification de connexion, les adresses IP, les niveaux de sécurité, les routes statiques ainsi que le routege avec ebgp, les listes d'accès(ACL), l'accès SSH, le NTP, le client DNS, la journalisation 

- **Configuration des ISPs (ISP1 et ISP2) :**
Spécifie la configuration des adresses IP, les paramètres eBGP, la configuration NAT, la configuration DNS et les mesures de sécurité. 
## 4. Dépannage et surveillance :

Ce document propose des étapes de dépannage et des techniques de surveillance pour le routeur de bordure et les ISPs. Cela comprend la vérification de l'état des connexions, la surveillance du trafic Internet, et la résolution des problèmes de connectivité.

## 5. Mesures de sécurité :
Les mesures de sécurité mises en œuvre pour le routeur Edge et les ISPs comprennent les listes de contrôle d'accès (ACL), l'authentification, le chiffrement des données, et la surveillance des logs pour détecter les activités suspectes.
## 6. Conclusion

Le routeur (Edge) et les fournisseurs de services Internet(ISPs) sont des éléments essentiels de l'infrastructure réseau d'une entreprise. En mettant en œuvre des configurations et des services appropriés, l'entreprise peut garantir la disponibilité, la sécurité et les performances nécessaires pour répondre à ses besoins opérationnels.
