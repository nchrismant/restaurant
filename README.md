# Restaurant intelligent — Self-service, Data & Vision par ordinateur

Ce projet vise à aider la gestion d’un restaurant de type self-service via une **solution intelligente** combinant :

- traitement d’images (reconnaissance des plats / plateaux),  
- gestion et traitement des données,  
- pipelines ETL via **Talend**,  
- interface graphique cliente via PyQt6,  
- analyse et recommandations basées sur les données collectées.

Projet réalisé en groupe (5 personnes).  

---

## 📌 Table des matières

- [Restaurant intelligent — Self-service, Data \& Vision par ordinateur](#restaurant-intelligent--self-service-data--vision-par-ordinateur)
  - [📌 Table des matières](#-table-des-matières)
  - [🎯 Objectifs du projet](#-objectifs-du-projet)
  - [🧩 Structure du projet](#-structure-du-projet)
  - [🚀 Installation \& Déploiement](#-installation--déploiement)
    - [Prérequis](#prérequis)
    - [Étapes d’installation](#étapes-dinstallation)
  - [🛠️ Technologies \& Outils utilisés](#️-technologies--outils-utilisés)
  - [👥 Auteurs \& Licence](#-auteurs--licence)

---

## 🎯 Objectifs du projet

Le projet a pour but de :

- Permettre la détection / reconnaissance automatique d’images : identifier les plats ou le contenu d’un plateau sur une image.  
- Centraliser les données via un pipeline ETL (Talend) pour les traitements, nettoyages, agrégations.  
- Fournir une interface utilisateur (application desktop via PyQt6) pour visualiser les données, résultats d’analyse et recommandations.  
- Combiner data engineering, computer vision et interface utilisateur pour un système “intelligent” de gestion de restaurant self-service.

---

## 🧩 Structure du projet

```text
/ (racine)
├── Data/ # Partie Data
    ├── BD/ # Création des éntrées des la base de données
    ├── Applications/ # Algorithmes de recommendations
    └── Tests/
├── Image/ Partie traitement d’images / vision par ordinateur
    ├── calibrage/ # Calibrage de la caméra
    ├── test_opencv/
    └── tracking/ # Algorithmes de tracking
├── Talend project/ # Datasets, Scripts sql de création de la base de données et Projet Talend pour transformation / nettoyage / ingestion de données
└── pyqt6/ # Interface graphique client en PyQt6 (visualisation, interaction)
    ├── Final_app/ # Application du restaurant
    └── PyQt_test/
```

## 🚀 Installation & Déploiement

### Prérequis  

- Serveur web PHP + MySQL (ou compatible)  
- Possibilité d’utiliser composer (selon la configuration)  

### Étapes d’installation  

1. Cloner le dépôt :

   ```bash
   git clone https://github.com/nchrismant/restaurant.git
   cd restaurant
   ```

2. Importer la base de données MySQL à partir du fichier `Talend project/ddl.sql`.
3. Lancer le projet Talend : ouvrir le projet Talend `Talend project/PIPO_RESTO.zip` avec Talend Open Studio, puis exécuter pour ingérer / transformer les données.
4. Lancer le script `Talend project/requetes.sql` pour compléter la base de données.
5. Déployer les fichiers sur votre serveur (ex : via FTP, SFTP ou un hébergement type Alwaysdata).
6. Lancer l’interface graphique (PyQt6)

    ```python
    python pyqt6/Final_app/main.py
    ```

7. Pour utiliser les scripts de traitement d’images : exécuter les scripts dans `Image/`.

---

## 🛠️ Technologies & Outils utilisés

| Technologie         | Rôle              |
| ------------------- | ----------------- |
| **MySQL**           | Base de données |
| **Talend**          | ETL |
| **Python**          | Application du restaurant et traitement d'images |
| **C** & **C++**               | Traitement d'images |

---

## 👥 Auteurs & Licence

- **CHRISMANT Nathan** — Étudiant Master IISC - SIC 1ère année, Cergy Paris Université.
- **GHEZIL Achref** — Étudiant Master IISC - SIC 1ère année, Cergy Paris Université.
- **KUCHLER Ulysse** — Étudiant Master IISC - SIC 1ère année, Cergy Paris Université.
- **LEMARCHAND Jonathan** — Étudiant Master IISC - SIC 1ère année, Cergy Paris Université.
- **SAOULI Imad Eddine** — Étudiant Master IISC - SIC 1ère année, Cergy Paris Université.

Ce projet est distribué sous licence Open Source Libre.
