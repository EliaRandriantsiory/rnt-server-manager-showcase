# RNT Server Manager — Administration Linux depuis le navigateur

> Une interface web pour superviser un serveur, gérer les partages réseau et suivre un parc informatique.

**Domaines :** Backend Python · Administration Linux · Supervision · Application web

## Le besoin

L'administration quotidienne d'un serveur implique plusieurs outils : commandes système, configuration des partages, consultation des journaux et suivi du matériel. Ces opérations sont difficiles à réaliser pour des utilisateurs peu familiers du terminal.

RNT Server Manager regroupe ces tâches dans une interface web destinée à un environnement administré.

## Périmètre de réalisation

- API backend intégrant des services Linux.
- Interface React pour les opérations courantes.
- Flux en temps réel pour la supervision et les journaux.
- Inventaire des équipements et gestion des accès applicatifs.

## Fonctionnalités

| Module | Capacités |
|---|---|
| Tableau de bord | Suivi CPU, mémoire, disque, réseau et durée de fonctionnement |
| Partages Samba | Création, modification et suppression de partages ; droits de lecture et d'écriture |
| Utilisateurs | Gestion des comptes Linux et Samba, mots de passe et groupes |
| Services | Consultation de l'état, démarrage, arrêt et redémarrage des services autorisés |
| Journaux | Consultation, recherche, filtrage et suivi des logs en direct |
| Parc informatique | Inventaire, affectations, garanties et suivi de l'état des équipements |

## Exemple de parcours

Un gestionnaire consulte la charge du serveur, recherche un équipement dans l'inventaire, puis vérifie l'état d'un service. Si une intervention est nécessaire, il consulte les journaux correspondants et utilise les actions disponibles dans l'interface.

Ce parcours illustre les fonctions de l'application, sans exposer d'équipement ni d'environnement réel.

## Architecture technique

| Couche | Technologies |
|---|---|
| Frontend | React 18, Vite |
| API | Python, FastAPI |
| Persistance | SQLAlchemy, SQLite |
| Authentification | JWT, bcrypt |
| Temps réel | WebSocket |
| Intégration système | systemd, journald, Samba |
| Environnement | Ubuntu Linux |

L'interface communique avec l'API pour les opérations courantes et reçoit les métriques et journaux via WebSocket. Le backend relie les fonctions applicatives aux services du système.

## Points d'ingénierie

- **Temps réel :** actualiser les métriques et les logs sans recharger les pages.
- **Intégration Linux :** convertir les opérations système en actions compréhensibles dans l'interface.
- **Encadrement des actions :** limiter les services pilotables et demander confirmation pour les opérations concernées.
- **Gestion de parc :** structurer les équipements par type, site et état.
- **Maintenance :** prévoir une installation scriptée et une gestion par systemd.

Les mécanismes d'authentification et de limitation des actions font partie de la conception documentée ; cette présentation ne revendique pas un audit de sécurité indépendant.

## Ce que ce projet démontre

Un travail à la jonction du développement applicatif et de l'infrastructure : API Python, interface React, communication en temps réel, persistance des données et intégration des outils Linux.

L'apport principal est de réunir supervision, administration et inventaire dans une même interface.

## À propos

Projet présenté par [Elia Randriantsiory](https://github.com/EliaRandriantsiory).

Ce dépôt est une **présentation de portfolio**. Il ne contient pas le code source de l'application, ni de données métier, de configuration de production ou d'identifiants. Les technologies tierces restent la propriété de leurs auteurs respectifs.

### Autres réalisations

- [Odoo ERP — Personnalisation métier](https://github.com/EliaRandriantsiory/odoo-erp-showcase)
- [RNT Server Manager — Administration Linux](https://github.com/EliaRandriantsiory/rnt-server-manager-showcase)
- [Fanavotana — Plateforme communautaire](https://github.com/EliaRandriantsiory/fanavotana-showcase)
