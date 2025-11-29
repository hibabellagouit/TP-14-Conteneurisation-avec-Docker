# 🎯 Objectif du TP

Ce travail pratique a pour but d’apprendre à déployer une application Spring Boot dans des conteneurs Docker, en comprenant les concepts fondamentaux de la containerisation et de l’orchestration multi-conteneurs.

À la fin du TP, l’étudiant sera capable de :

Construire une image Docker à partir d’une application Spring Boot.

Exécuter une application dans un conteneur Docker.

Configurer des variables d’environnement dans un conteneur.

Déployer une base de données MySQL dans un second conteneur.

Faire communiquer plusieurs conteneurs via Docker Compose.

Gérer les données persistantes avec des volumes.

# 🧱 1. Préparation du Projet Spring Boot

L’étudiant crée une application Spring Boot incluant Web, JPA, MySQL et Lombok.
Une configuration de base est ajoutée pour définir la connexion à MySQL.

L’application est ensuite compilée et testée localement pour vérifier son bon fonctionnement avant la containerisation.


📦 2. Création de l’Image Docker

Un fichier Dockerfile est ajouté pour décrire :

l’image de base Java utilisée ;

le répertoire de travail dans le conteneur ;

la copie du fichier exécutable de l’application ;

le port exposé par l’application ;

la commande exécutée au démarrage.

L’image Docker est ensuite construite et vérifiée.

▶️ 3. Exécution de l’Application dans un Conteneur

Le conteneur est lancé en exposant le port de l’application vers la machine hôte.
L’étudiant apprend à :

démarrer un conteneur en arrière-plan ;

consulter les logs ;

vérifier l’accessibilité de l’application dans un navigateur ;

arrêter et supprimer des conteneurs.

🗄️ 4. Mise en Place de MySQL dans un Conteneur

Une base de données MySQL est ensuite déployée dans un second conteneur.
L’étudiant découvre :

comment définir le mot de passe root ;

comment exposer le port MySQL ;

comment persister les données sur l’hôte via les volumes.

<img width="1366" height="728" alt="Containers - Docker Desktop 29_11_2025 00_56_11" src="https://github.com/user-attachments/assets/cb5543fb-80c8-4914-ad07-3d5ffbdee2b6" />

🔗 5. Orchestration avec Docker Compose

Docker Compose est utilisé pour lancer plusieurs services :

l’application Spring Boot ;

le serveur MySQL.

Les services sont liés entre eux grâce à un réseau interne.
Docker Compose permet :

de démarrer tous les services avec une seule commande ;

d’afficher les logs combinés ;

de gérer proprement l’arrêt des conteneurs.

✔️ 6. Vérifications et Tests

L’étudiant valide que :

l’application communique correctement avec MySQL ;

les données persistent après redémarrage ;

les ports nécessaires sont bien exposés ;

la configuration de l’environnement fonctionne.

