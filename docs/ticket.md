---
sidebar_position: 8
---

# Support

## Trello
Afin de gérer les éventuelles requêtes ou rapports d'erreur des clients, utilisant notre application, nous avons décidé d'établir un tableau Kanban les répertoriant sur le site Trello.
Trello disposant d'une API, il nous est facile d'ordonner chaque rapport de manière visuelle dans différentes listes d'avancements.

## Trello API
En suivant l'introduction de la documentation de Trello : https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/

Nous crééons une **APIKey** dans notre espace d'administration des Power-ups tout en indiquant notre espace de travail pour intéréagir avec le tableau voulu.
Une fois notre APIKey créée nous devons récupérer son **token** pour tester l'endpoint avec le logiciel Insomnia.

Pour tester notre endpoint il nous manque un élément, il s'agit du **boardId** qui correspond à l'id de notre tableau, afin de le récupérer il nous suffit de rajouter ".json" au lien de notre tableau et de récupérer le premier paramètre id affiché.

Voici la structure de l'endpoint pour récupérer (GET) notre tableau :
https://api.trello.com/1/boards/{boardId}?key={APIKey}&token={token}

Ajouter une carte dans une liste du tableau est possible seulement si le **listId** est mentionné, cet id correspond à l'id de la liste dans laquelle la carte va être créée.
L'endpoint de création de carte (POST) :
https://api.trello.com/1/cards?idList={listId}&key={APIKey}&token={token}

La création de carte peut être approfondie à l'aide de paramètres que l'on peut retrouver sur la documentation :
https://developer.atlassian.com/cloud/trello/rest/api-group-cards/
