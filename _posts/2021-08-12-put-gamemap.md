---
category: gamemap
url_path: '/game_maps'
title: 'edit gamemap'
type: 'PUT'

layout: null
---
## Update gameMaps request (methode : PUT)
Required Role :
* ROLE_SUPERADMIN

To Update gameMaps you need to use endpoint /game_maps and its id.
Example :
```
http://127.0.0.1:8000/game_maps/1
```
json 
```{
  "map": "string",
  "difficulty": "string"
}```
## Successful response :
*Response body*
```{
    "id": 2,
    "map": "string",
    "difficulty": "string",
    "games": []
}```

## Unsuccessful response :
*Response body*
```{
  {
    "code": 401,
    "message": "Unable to load an user with property \"gameMaps\" = \"\". If the user identity has changed, you must renew the token. Otherwise, verify that the \"lexik_jwt_authentication.user_identity_field\" config option is correctly set."
}```
fix : the given id does not exist. use existed id.

## Unsuccessful response :
*Response body*
```{
    "message": "map : string already exist",
    "map": "string",
    "error": "not-unique"
}```
fix : map is used . use unqiue one .

## Unsuccessful response :
*Response body*
```{
 "propertyPath": "difficulty",
  "message": "This value should not be blank.",
  "code": "c1051bb4-d103-4f74-8988-acbcafc7fdc3"
}```
fix : This value of difficulty should not be blank .