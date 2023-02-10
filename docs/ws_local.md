---
sidebar_position: 4
---

# Service WS local 

## Description

Un serveur node qui utilise les libraires redis et ws. La librairie redis sert à requeter la base de données et à subscribe au broker redis. La librairie ws sert à se connecter au serveur WS cloud, à chaque message sur le broker redis le message est ensuite envoyer au cloud pour mettre en base la données.

La librairie ws sert aussi de queue en cas de perte de connexion.

Le dockerfile utilise l'image node:alpine, copie le package.json et lance un npm install.

## Commande docker utile
Pour build l'image ws-local:
```bash
docker build -t ws-local .
```
Pour run l'image ws-local :
```bash
docker run ws-local
```