---
category: user
url_path: '/users'
title: 'delete user'
type: 'DELETE'

layout: null
---
## delete users request (methode : DELETE)
Required Role :
* ROLE_SUPERADMIN

To delete user you need to use endpoint /users and his id.
Example :
```
http://127.0.0.1:8000/users/1
```

## Successful response :
*Response body*
```{
  UserId
}```

## Unsuccessful response :
*Response body*
```{
    "code": 401,
    "message": "Unable to load an user with property \"username\" = \"admin\". If the user identity has changed, you must renew the token. Otherwise, verify that the \"lexik_jwt_authentication.user_identity_field\" config option is correctly set."
}```
fix : the given id does not exist. use existed id. 
