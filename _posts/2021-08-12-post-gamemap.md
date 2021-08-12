---
category: gamemap
url_path: '/game_maps'
title: 'post gamemap'
type: 'POST'

layout: null
---
## make GameMap request (methode : POST)
Required Role :
* ROLE_SUPERADMIN

To make gameMap you need to use endpoint /game_maps.
Example :
```
http://127.0.0.1:8000/game_maps
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