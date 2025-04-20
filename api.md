---
layout: default
permalink: /api/
---

# API

## `/`
**Method:** any

Redirect to the link creation page *set by the server administrator*

### Request
```
GET / HTTP/2
Host: pyt.pp.ua

```

### Response
```
HTTP/2 301 Moved Permanently
Location: //url.pavliktt.pp.ua/

```

## `/new`
**Method:** POST, *(GET, HEAD)*

Create a short link.

### Request
```
POST /new HTTP/2
Host: pyt.pp.ua

{
    "url": "https://example.com/",
    "mode": "normal"
}
```

`url` &mdash; URL that you want to shorten\
`mode` &mdash; Length of output link *(optional)*

#### Available modes:
The available at this moment modes are:

1. short: 4 characters
2. normal: 6 characters (default)
3. long: 10 characters

### Response
```
HTTP/2 200 OK
Content-Type: text/json
Content-Length: 34

{"url":"https://pyt.pp.ua/xxxxxx"}
```

## `/meta/{link id}`
**Method:** GET, *(HEAD)*

Get link's metadata

### Request
```
GET /meta/{link id} HTTP/2
Host: pyt.pp.ua

```

### Response
```
HTTP/2 200 OK
Content-Type: application/json
Content-Length: 52

{"url":"https://example.com","created":946677600000}
```

`url` - target URL\
`created` - creation date as a UNIX timestamp with milliseconds
