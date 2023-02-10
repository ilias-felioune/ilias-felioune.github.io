---
sidebar_position: 4
---

# API Manager

## Description

Cette partie se compose de deux services NodeJs avec Express qui serviront l'une à requeter la base de données locale de Redis et l'autre la base de donnée Cloud InfluxDb. Ces deux services seront appelés depuis l'application mobile Flutter, la base de donnée Cloud sera appelée en priorité et si celle-ci ne peut pas être requeter, la base de donnée locale sera requeté à la place.
#
Le dockerfile utilise l'image node:alpine, copie le package.json et lance un npm install.

## Routes Cloud:
- /get_users
- /get_sensors
- /get_rooms
- /get_buildings

## Routes Locale:

## Commandes docker utiles
Pour build l'image api-manager-local:
```bash
docker build api-manager-local .
```
Pour build l'image api-manager-cloud:
```bash
docker build api-manager-cloud .
```
Pour run l'image api-manager-locale :
```bash
docker run api-manager-local
```
Pour run l'image api-manager-cloud :
```bash
docker run api-manager-cloud
```