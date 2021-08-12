---
category: player
url_path: '/players'
title: 'delete player'
type: 'DELETE'

layout: null
---
## delete players request (methode : DELETE)
Required Role :
* ROLE_SUPERADMIN
* ROLE_OPERATOR
* ROLE_RESELLER

** one role is required.

To delete a player you need to use endpoint /players and his id.
Example :
```
http://127.0.0.1:8000/players/1
```
## Successful response :
*Response body*
```{
  playerId
}```

## Unsuccessful response :
*Response body*
```{
  "code": 401,
  "message": "Unable to load an user with property \"player\" = \"string\". If the user identity has changed, you must renew the token. Otherwise, verify that the \"lexik_jwt_authentication.user_identity_field\" config option is correctly set."
}```
fix : the given id does not exist. use existed id. 
