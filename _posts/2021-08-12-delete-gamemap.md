---
category: gamemap
url_path: '/game_maps'
title: 'delete gamemap'
type: 'DELETE'

layout: null
---
## delete gameMaps request (methode : DELETE)
Required Role :
* ROLE_SUPERADMIN

To delete gameMaps you need to use endpoint /game_maps and its id.
Example :
```
http://127.0.0.1:8000/game_maps/1
```

## Successful response :
*Response body*
```{
  gameMapsId
}```

## Unsuccessful response :
*Response body*
```{
  {
    "code": 401,
    "message": "Unable to load an user with property \"gamemaps\" = \"\". If the user identity has changed, you must renew the token. Otherwise, verify that the \"lexik_jwt_authentication.user_identity_field\" config option is correctly set."
  }
}```
fix : the given id does not exist. use existed id.