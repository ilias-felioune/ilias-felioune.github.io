---
sidebar_position: 3
---

# Module redis

## Description

Le dockerfile utilise l'image redis/redis-stack:latest, et il permet de monter le fichire de conf dans le container. Le fichier de conf permet de publier sur le broker a chaque modification en base grace à cette attribut :
```js
notify-keyspace-events KEA
```
A part ca l'image redis n'est pas custom.

## Commande docker utile

Pour build l'image redis :
```bash
docker build -t redis-local .
```
Pour run l'image redis :
```bash
docker run -p 127.0.0.1:6379:6379 redis-local
```
