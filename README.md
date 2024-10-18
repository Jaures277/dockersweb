# TP Docker #2

Ce projet contient la solution pour le TP Docker #2. Le projet est organisé en plusieurs étapes, chaque étape ayant ses propres répertoires et fichiers.

## Structure du projet

Le projet est structuré de la manière suivante :

- **etape1/** : Contient les fichiers pour l'étape 1 avec les deux containers HTTP et SCRIPT.
- **etape2/** : Contient les fichiers pour l'étape 2 avec trois containers (HTTP, SCRIPT, et DATA).
- **etape3/** : Contient les fichiers pour l'étape 3 avec un site Wordpress installé.
- **etape4/** : Contient la configuration Docker Compose pour l'étape 3.

---

## Étapes du TP

### Étape 1 : Mise en place de deux containers
Dans cette première étape, deux containers sont créés :

1. **HTTP** : Un container avec un serveur HTTP qui écoute sur le port 8080.
2. **SCRIPT** : Un container avec PHP-FPM pour exécuter du code PHP.

Un fichier `index.php` est placé dans le répertoire `/app` du container HTTP. Il affiche la page `phpinfo()`.

#### Test :
Accédez à l'adresse suivante dans un navigateur pour vérifier l'exécution de `phpinfo()` :


### Étape 2 : Ajout d'un container de base de données
Trois containers sont maintenant en place :

1. **HTTP** : Serveur HTTP sur le port 8080.
2. **SCRIPT** : PHP-FPM pour exécuter du code PHP.
3. **DATA** : Serveur de base de données (MariaDB, MySQL, ou PostgreSQL).

Un fichier `test_bdd.php` exécute des opérations CRUD (Create, Read, Update, Delete) sur la base de données. À chaque rafraîchissement de la page, les données sont modifiées.

#### Test :
Accédez à l'adresse suivante dans un navigateur pour vérifier les interactions avec la base de données :


### Étape 3 : Installation de Wordpress
Trois containers sont utilisés :

1. **HTTP** : Serveur HTTP sur le port 8080.
2. **SCRIPT** : PHP-FPM pour exécuter le code PHP.
3. **DATA** : Serveur de base de données pour Wordpress.

Le contenu de l'application PHP est remplacé par un site Wordpress complet. Vous pouvez accéder à l'interface d'installation de Wordpress via un navigateur.

#### Test :
Accédez à l'URL suivante pour lancer l'installation de Wordpress :


### Étape 4 : Conversion en Docker Compose
Dans cette étape, la configuration manuelle des containers est remplacée par un fichier `docker-compose.yml` pour simplifier le déploiement.

#### Test :
Lancez Docker Compose avec la commande suivante :

```bash
docker-compose up
