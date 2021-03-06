---
title: Polycloud API Reference

language_tabs:
  - shell

search: true
---

# Introduction

This is the Polycloud API documentation.

# Languages

## Get All Languages

```shell
curl "http://example.com/languages" -H "Accept: application/vnd.polycloud;ver=1+json"
```

> The above command returns JSON structured like this:

```json
{
  "languages": [
    {
      "id": 1,
      "title": "Ruby",
      "snippets_ids": [1, 5]
    },
    {
      "id": 1,
      "title": "Python",
      "snippets_ids": [2, 3, 4]
    }
  ]
}
```

This endpoint retrieves all languages.

### HTTP Request

`GET http://example.com/languages`

## Get a Specific Language

```shell
curl "http://example.com/languages/3" -H "Accept: application/vnd.polycloud;ver=1+json"
```

> The above command returns JSON structured like this:

```json
{
  "language": {
    "id": 1,
    "title": "Ruby",
    "snippets_ids": [1, 5]
  }
}
```

This endpoint retrieves a specific language.

### HTTP Request

`GET http://example.com/languages/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the language to retrieve


## Create a new language

> The above command returns JSON structured like this:

```json
{
  "language": {
    "id": 3,
    "title": "Java",
    "snippets_ids": []
  }
}
```

This endpoint creates a new language.

### HTTP Request

`POST http://example.com/languages`

### URL Parameters

Parameter | Description
--------- | -----------
TITLE | The title of the new language


## Update an existing language

> The above command returns JSON structured like this:

```json
{
  "language": {
    "id": 3,
    "title": "Java",
    "snippets_ids": [6, 8]
  }
}
```

This endpoint updates an existing language.

### HTTP Request

`PATCH/PUT http://example.com/languages/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
TITLE | new title of the language


## Destroy a language

> The above command returns JSON structured like this:

```json
{
  "language": {
    "id": 3,
    "title": "Java",
    "snippets_ids": []
  }
}
```

This endpoint destroys an existing language.

### HTTP Request

`DELETE http://example.com/languages/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the language to destroy

# Snippets

## Get All Snippets

```shell
curl "http://example.com/snippets" -H "Accept: application/vnd.polycloud;ver=1+json"
```

> The above command returns JSON structured like this:

```json
{
  "snippets": [
    {
      "id": 1,
      "user_id": 1,
      "content": "Hello World",
      "language_id": 1
    },
    {
      "id": 2,
      "user_id": 1,
      "content": "Hello World",
      "language_id": 2
    }
  ]
}
```

This endpoint retrieves all snippets.

### HTTP Request

`GET http://example.com/snippets`

## Get a Specific Snippet

```shell
curl "http://example.com/snippets/3" -H "Accept: application/vnd.polycloud;ver=1+json"
```

> The above command returns JSON structured like this:

```json
{
  "snippet": {
    "id": 1,
    "user_id": 1,
    "content": "Hello World",
    "language_id": 1
  }
}
```

This endpoint retrieves a specific snippet.

### HTTP Request

`GET http://example.com/snippets/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the snippet to retrieve

## Create a new snippet

> The above command returns JSON structured like this:

```json
{
  "snippet": {
    "id": 1,
    "user_id": 1,
    "content": "Hello World",
    "language_id": 1
  }
}
```

This endpoint creates a new snippet.

### HTTP Request

`POST http://example.com/snippets`

### URL Parameters

Parameter | Description
--------- | -----------
CONTENT | The content of the new snippet.
LANGUAGE_ID | The id of the language in which the snippet is written.


## Update an existing snippet

> The above command returns JSON structured like this:

```json
{
  "snippet": {
    "id": 1,
    "user_id": 1,
    "content": "Hello World",
    "language_id": 1
  }
}
```

This endpoint updates an existing snippet.

### HTTP Request

`PATCH/PUT http://example.com/snippets/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
CONTENT | The new content of the snippet
LANGUAGE_ID | The id of the language in which the snippet is written.


## Destroy a snippet

> The above command returns JSON structured like this:

```json
{
  "snippet": {
    "id": 1,
    "user_id": 1,
    "content": "Hello World",
    "language_id": 1
  }
}
```

This endpoint destroys an existing snippet.

### HTTP Request

`DELETE http://example.com/snippets/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the snippet to destroy
