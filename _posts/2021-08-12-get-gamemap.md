---
category: gamemap
url_path: '/game_maps'
title: 'get gamemap'
type: 'get'

layout: null
---
## Parameters
All parameters that are available to the gameMap

| Name  | Value   | Explanation    | requirment |
|-------------|-------------|-------------|-------------|
| map      |varchar| all the different maps  | required and unique |
| difficulty     |varchar| the difficulty of the map    |required |

## get gameMaps request (methode : GET)
One role is Required :
* ROLE_SUPERADMIN
* ROLE_OPERATOR
* ROLE_RESELLER

To get gameMaps you need to use endpoint /game_maps.
Example :
```
http://127.0.0.1:8000/game_maps
```
## Successful response :
*Response body*
```{
"@context": "/contexts/GameMap",
    "@id": "/game_maps",
    "@type": "hydra:Collection",
    "hydra:member": [
        {
            "@id": "/game_maps/1",
            "@type": "GameMap",
            "id": 1,
            "map": "crazy",
            "difficulty": "medium",
            "games": [
                "/games/1",
            ]
        }
}```
