---
title: Stats/{stats_id}
keywords: Youthweb-API, Resource, Stats
tags: [endpoint]
summary: "Mit diesem Endpoint können statistische Daten zu bestimmten Bereichen ermittelt werden."
sidebar: api_sidebar
permalink: api_endpoint_stats.html
folder: api
---

Dieser Endpoint liefert Statistiken zu Usern, Gruppen und Forum.

## Read

### Request

```
GET https://api.youthweb.net/stats/account
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json
```

### Permissions

Für diesen Endpoint wird kein Access-Token benötigt.

### Parameter

Für den Request können keine Parameter angegeben werden.

### Response

```
Status: 200 OK
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json

{
    "data": {
        "type": "stats",
        "id": "account",
        "attributes": {
            "user_total": 5503,
            "user_total_female": 2831,
            "user_total_male": 2672,
            "user_online": 74,
            "user_online_24h": 629,
            "user_online_7d": 1035,
            "user_online_30d": 1600,
            "userpics": 3441
        },
        "links": {
            "self": "/stats/account"
        }
    }
}
```

### Felder

Siehe [hier](http://docs.youthweb.apiary.io/#reference/stats) für mehr Infos zur Bedeutung der einzelnen Felder.

## Create

Du kannst mit diesem Endpoint nichts erstellen.

## Delete

Du kannst mit diesem Endpoint nichts löschen.

## Update

Du kannst mit diesem Endpoint nichts ändern.

## Beziehungen

keine

## Beispiele

### Beispiel 1: Account Statistiken

**Request**

```
GET https://api.youthweb.net/stats/account
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json
```

**Response**

```
Status: 200 OK
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json

{
    "data": {
        "type": "stats",
        "id": "account",
        "attributes": {
            "user_total": 5503,
            "user_total_female": 2831,
            "user_total_male": 2672,
            "user_online": 74,
            "user_online_24h": 629,
            "user_online_7d": 1035,
            "user_online_30d": 1600,
            "userpics": 3441
        },
        "links": {
            "self": "/stats/account"
        }
    }
}
```

### Beispiel 2: Foren Statistiken

**Request**

```
GET https://api.youthweb.net/stats/forum
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json
```

**Response**

```
Status: 200 OK
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json

{
    "data": {
        "type": "stats",
        "id": "forum",
        "attributes": {
            "authors_total": 1480,
            "threads_total": 2094,
            "posts_total": 121387
        },
        "links": {
            "self": "/stats/forum"
        }
    }
}
```

### Beispiel 3: Gruppen Statistiken

**Request**

```
GET https://api.youthweb.net/stats/groups
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json
```

**Response**

```
Status: 200 OK
Accept: application/vnd.api+json, application/vnd.api+json; net.youthweb.api.version=0.13
Content-Type: application/vnd.api+json

{
    "data": {
        "type": "stats",
        "id": "groups",
        "attributes": {
            "groups_total": 614,
            "users_total": 2073
        },
        "links": {
            "self": "/stats/groups"
        }
    }
}
```

{% include links.html %}
