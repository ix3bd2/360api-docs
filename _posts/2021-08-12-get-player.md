---
category: player
url_path: '/players'
title: 'get player'
type: 'get'

layout: null
---
## Parameters
All parameters that are available to the players

| Name  | Value   | Explanation    | requirment |
|-------------|-------------|-------------|-------------|
| game      |int| relation with game  | required |
| nickName      |varchar| nickname of the player| not required and unqiue |
| code      |varchar| code to login | not required and unqiue |
| idOrderItemPlayer      |varchar| od for player | required and unique |

## Get players request (methode : GET)
Required Role :
* ROLE_SUPERADMIN
* ROLE_OPERATOR
* ROLE_RESELLER

** one role is required.

To get players you need to use endpoint /players.
Example :
```
http://127.0.0.1:8000/players
```