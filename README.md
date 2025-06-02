# 🐳 Symfony 7 + Docker Setup

> ⚙️ Setup inspiré de l’article : Symfony 7 avec Docker - citizenz.info

---

## 📁 Fichiers de configuration Docker

- `compose.yml` – Configuration principale des services Docker  
- `Dockerfile` – Image PHP personnalisée avec extensions nécessaires  
- `php.ini` – Configuration PHP personnalisée  
- `nginx.conf` – Configuration du serveur Nginx  
- `README.md` – Ce fichier 😉

---

## 🚀 Installation de Symfony

```symfony new --webapp app```

> Cela génère un projet Symfony 7 dans le dossier `app/`.

---

## 🐋 Commandes Docker

### ▶️ Lancer les conteneurs

```docker-compose up -d```

### ⏹️ Arrêter les conteneurs

```docker-compose stop```

## 🧹 Supprimer les conteneurs

```docker-compose down```

## 🌐 Accès aux services locaux

| Service       | URL                    |
|---------------|------------------------|
| Symfony       | http://127.0.0.1:8080  |
| PhpMyAdmin    | http://127.0.0.1:8081  |
| Mailpit       | http://127.0.0.1:8025  |

---

## 🛠️ Dépannage : permissions sur `var/cache` et `var/log`

En cas de problèmes d'accès ou d'écriture :

- ```docker-compose exec php chmod -R 777 var/cache```
- ```docker-compose exec php chmod -R 777 var/log```

> ⚠️ À utiliser uniquement en environnement de développement.

---

## 🛠️ Dépannage : volume `db_data`

- ```docker volume ls```
- ```docker volume rm docker-sf_db_data```