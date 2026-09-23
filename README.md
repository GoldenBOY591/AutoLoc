# AutoLoc

**Plateforme de gestion de location de véhicules multi-agences**

Projet réalisé dans le cadre de l'unité **UP ASI — Architecture des Systèmes d'Information** (ESPRIT).

> Statut : **README v0 — Atelier 0 (mise en place de l'environnement)**

---

## 1. Objectifs du projet

AutoLoc a pour but de concevoir et développer une application web de gestion de location de véhicules pour un réseau de plusieurs agences. La plateforme doit permettre de :

- **Centraliser** la gestion du parc de véhicules de toutes les agences ;
- **Faciliter la réservation** d'un véhicule par les clients (recherche, disponibilité, réservation, annulation) ;
- **Suivre le cycle de location** : retrait, restitution, état du véhicule, facturation ;
- **Donner une vue de pilotage** aux responsables d'agence et à l'administrateur (statistiques, gestion des utilisateurs et des agences) ;
- **Exposer une API REST** documentée, testable avec Postman et Swagger UI.

Objectifs pédagogiques : appliquer une architecture en couches avec Spring Boot, la persistance avec Spring Data JPA, les tests automatisés et le travail collaboratif avec Git.

---

## 2. Acteurs identifiés

| Acteur | Rôle |
|---|---|
| **Client** | Recherche et réserve un véhicule, consulte l'historique de ses locations |
| **Agent d'agence** | Traite les réservations au quotidien, enregistre les retraits et restitutions |
| **Responsable d'agence** (Manager) | Gère le parc et l'activité de son agence, consulte les indicateurs |
| **Administrateur** | Administre la plateforme : agences, utilisateurs, rôles, paramètres |

### Premiers cas d'utilisation (à affiner)

**Client**
- Créer un compte et s'authentifier
- Rechercher un véhicule (agence, dates, catégorie)
- Réserver un véhicule
- Annuler une réservation
- Consulter l'historique de ses locations

**Agent d'agence**
- Créer ou modifier une réservation au comptoir
- Enregistrer le retrait d'un véhicule
- Enregistrer la restitution et constater l'état du véhicule
- Établir la facture d'une location

**Responsable d'agence**
- Gérer les véhicules de l'agence (ajout, statut, maintenance)
- Gérer les agents de l'agence
- Consulter les statistiques de l'agence

**Administrateur**
- Gérer les agences
- Gérer les utilisateurs et leurs rôles
- Consulter les statistiques globales de la plateforme

---

## 3. Stack technique

| Catégorie | Outils |
|---|---|
| Langage / Build | Java 17, Maven |
| Framework | Spring Boot, Spring Data JPA, Spring MVC, Spring AOP, Spring Scheduler |
| Base de données | MySQL (développement), H2 en mémoire (tests) |
| Productivité | Lombok, SLF4J/Logback, MapStruct (optionnel) |
| Documentation API | springdoc-openapi (Swagger UI) |
| Tests | JUnit 5, Mockito, MockMvc, Jacoco |
| Qualité | SonarLint |
| Outillage | Git/GitHub, Postman, IntelliJ IDEA Ultimate |

---

## 4. Environnement de développement (Atelier 0)

| Élément | Version / Détail |
|---|---|
| JDK | Eclipse Temurin 17 |
| IDE | IntelliJ IDEA Ultimate (licence étudiante) |
| Base de données | MySQL/MariaDB via XAMPP, base `autoloc_db` (utf8mb4) |
| Client SGBD | phpMyAdmin |
| Client API | Postman, collection `AutoLoc-API` |
| Gestion de version | Git 2.47 + GitHub |

Création de la base :

```sql
CREATE DATABASE autoloc_db CHARACTER SET utf8mb4;
```

Les preuves de l'environnement fonctionnel se trouvent dans [`docs/screenshots/`](docs/screenshots/).

---

## 5. Équipe

| Nom | Rôle |
|---|---|
| Rayen Amri | *(à compléter)* |
| *(à compléter)* | *(à compléter)* |

---

## 6. Structure du dépôt

```
AutoLoc/
├── docs/
│   └── screenshots/    # preuves de l'environnement (Atelier 0)
├── .gitignore
└── README.md
```

*Le code source (projet Spring Boot) sera ajouté au fil des ateliers.*
