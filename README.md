# TP-32 Microservices - CI/CD avec Jenkins et SonarQube

## 📋 Description

Ce projet implémente une architecture de déploiement continue (CI/CD) utilisant **Jenkins** et **SonarQube** pour l'analyse de qualité de code dans un environnement microservices.

## 🏗️ Architecture

Le projet utilise Docker Compose pour orchestrer les services suivants :

- **SonarQube** : Plateforme d'analyse de qualité de code
- **PostgreSQL** : Base de données pour SonarQube
- **Jenkins** : Serveur d'intégration continue

## 🚀 Démarrage Rapide

### Prérequis

- Docker et Docker Compose installés
- Minimum 4GB de RAM disponible pour SonarQube

### Lancer SonarQube

```bash
docker-compose -f sonarqube-compose.yml up -d
```

### Accéder aux services

| Service | URL | Identifiants par défaut |
|---------|-----|------------------------|
| SonarQube | http://localhost:9999 | admin / admin |

## 📁 Structure du Projet

```
TP-32-Microservices-main/
├── jenkins2/                    # Configuration Jenkins
├── sonarqube-compose.yml        # Docker Compose pour SonarQube
└── README.md                    # Documentation
```

## ⚙️ Configuration

### SonarQube

Le fichier `sonarqube-compose.yml` configure :

- **Port** : 9999 (mappé sur le port 9000 interne)
- **Base de données** : PostgreSQL avec persistance des données
- **Credentials BD** : 
  - User: `sonar`
  - Password: `sonar_pass`
  - Database: `sonarqube`

## 🔧 Commandes Utiles

```bash
# Démarrer les services
docker-compose -f sonarqube-compose.yml up -d

# Arrêter les services
docker-compose -f sonarqube-compose.yml down

# Voir les logs
docker-compose -f sonarqube-compose.yml logs -f

# Vérifier le statut
docker-compose -f sonarqube-compose.yml ps
```

## 👤 Auteur

**Othmani Hasna**

## 📄 Licence

Ce projet est réalisé dans le cadre d'un TP académique.
