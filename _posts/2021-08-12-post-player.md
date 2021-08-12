---
category: player
url_path: '/players'
title: 'post player'
type: 'POST'

layout: null
---
## Make player request (methode : POST)
Required Role :
* ROLE_SUPERADMIN
* ROLE_OPERATOR
* ROLE_RESELLER

** one role is required.

To make a player you need to use endpoint /players.
Example :
```
http://127.0.0.1:8000/players
```
json 
```{
  "game": "games/1",
  "idOrderItemPlayer": "string"
}```
or
```{
  "game": "games/1",
  "nickName": "string",
  "idOrderItemPlayer": "string",
}```

## Successful response :
*Response body*
```{
  "id": 190,
  "game": "/games/1",
  "nickName": "string",
  "code": "655192",
  "idOrderItemPlayer": "string",
}```
## Unsuccessful response :
*Response body*
```{
  "message": "strasdsading is already in use",
  "error": "not-unique",
  "id": "strasdsading",
  "code": "655192"
}```
fix :use unqiue nickname or idOrderItemPlayer

## Unsuccessful response :
*Response body*
```{
  "hydra:description": "Item not found for \"games/123123\".",
}```
fix :games does not exist. use existing one.
