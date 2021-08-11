---
category: playerLogins
url_path: '/player_logins'
title: 'playerLogin'
type: 'POST'

layout: null
---

This method allows users to create a new thing.

### Request Example

```json
{
  "code": "string",
  "nickName": "string",
  "hints": 0,
  "progress": [
    "string"
  ],
  "teamName": "string",
  "startTime": "2021-04-12T09:27:28.694Z",
  "lastActionTime": "2021-04-12T09:27:28.694Z",
  "endTime": "2021-04-12T09:27:28.694Z",
  "penaltyTime": 0
}

### Successful Response


```json
{
    "message": "updated player",
    "nick_name": "string",
    "team_name": "string",
    "uid_game": "606340e4ba8e12.67383903",
    "secret_key": "901458786992",
    "start_time": {
        "date": "2021-04-12 09:27:28.694000",
        "timezone_type": 2,
        "timezone": "Z"
    },
    "last_action_time": {
        "date": "2021-04-12 09:27:28.694000",
        "timezone_type": 2,
        "timezone": "Z"
    },
    "end_time": {
        "date": "2021-04-12 09:27:28.694000",
        "timezone_type": 2,
        "timezone": "Z"
    },
    "progress": [
        "string"
    ]
}
```

### Unsuccessful Response (not-found)

```json
{
  "message": "Gamecode doesn't exist",
  "error": "not-found"
}
```

### Unsuccessful Response (not-unique)

```json
{
    "message": "Kokoka is already in use",
    "nick_name": "stringsd",
    "team_name": "string",
    "uid_game": "606340e4ba8e12.67383903",
    "secret_key": "901458786992",
    "error": "not-unique"
}
```
