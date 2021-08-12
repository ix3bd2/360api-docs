---
category: login
url_path: '/login_check'
title: 'login'
type: 'POST'

layout: null
---
## Parameters

| Name  | Value   | Explanation    | requirment |
|-------------|-------------|-------------|-------------|
| username            |varchar| your username | required |
| password      |varchar| your password  | required |

## Login : Request (methode :POST)
To login please use endpoint /login_check.
Example :
```
http://127.0.0.1:8000/login_check
```
## Login: Json
To login you need to send user informations to the api.
Example :
```{
    "username":"username",
    "password":"password"
}```

## Successful response :
```{
    "token": "Your token"
}```

## Unsuccessful response :
```{
    "code": 401,
    "message": "Invalid credentials."
}```
fix : Please Check if you are using the correct username and password.

## Importent token after a successful login :
Please import your token to the header(bearer).
Example :
```{
Authorization : bearer yourtoken
}```
 
## Unsuccessfully Imported token :
when you faild to import your token to the header .
Example error :
```{
    "code": 401,
    "message": "JWT Token not found"
}``` 
fix : Import token to the header .


## Expired token
Example expired error :
```{
    "code": 401,
    "message": "Expired JWT Token"
}``` 
fix : Relogin than import your token to the header
