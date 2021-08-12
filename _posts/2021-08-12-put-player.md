---
category: player
url_path: '/players'
title: 'edit player'
type: 'PUT'

layout: null
---
## Update player request (methode : PUT)
Required Role :
* ROLE_SUPERADMIN
* ROLE_OPERATOR
* ROLE_RESELLER

** one role is required.

To Update a player you need to use endpoint /players and his id.
Example :
```
http://127.0.0.1:8000/players/1
```

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
  "code": 401,
  "message": "Unable to load an user with property \"player\" = \"test\". If the user identity has changed, you must renew the token. Otherwise, verify that the \"lexik_jwt_authentication.user_identity_field\" config option is correctly set."
}```
fix : the given id does not exist. use existed id.