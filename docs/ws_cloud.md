---
sidebar_position: 5
---

# Service WS

## Description

Un conteneur node WebSocket qui permet d'echanger avec le local les différents changements en base de données. En fonction du message recu de la forme {commande,clé,valeur}, le serveur peut determiné à partir de la clé, vers quelle base la données doit être envoyé.

Le dockerfile utilise l'image node:alpine comme le WS local.

## Commande docker utile
Pour build l'image cloud :
```bash
docker build -t ws-cloud .
```
Pour run l'image cloud :
```bash
docker run -p 127.0.0.1:5000:3000 ws-cloud
```