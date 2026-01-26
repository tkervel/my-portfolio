---
sidebar_position: 6
sidebar_label: "API Documentation"
title: "API Documentation"
description: "A simple and fun exercise"
keywords:
  - API
  - Swagger
---

## 🧙‍♀️ Realm of the Elderlings API (Mock API)   
A fantasy-themed exercise to play around with API documentation.
Inspired by [Robin Hobb](https://en.wikipedia.org/wiki/Robin_Hobb)’s Realm of the Elderlings universe.

:::note
This mock API was created as a Technical Writing and Developer Experience exercise to demonstrate API design and documentation skills.
:::

## 🧭 Overview 
The Realm of the Elderlings API is a mock REST API that exposes resources from the world of FitzChivalry Farseer, including characters, Wit and Skill bonds, and assassin assignments.
It is implemented as a mock server using an OpenAPI 3.0 specification.

This project showcases:

    - API design 
    - OpenAPI specification writing
    - REST documentation
    - JSON modeling
    - Developer‑friendly structure and clarity

## 🔗 Base URL
This API uses multiple mock endpoints generated via [swagger.io](https://editor.swagger.io/).

The mock server is automatically generated from the OpenAPI specification:

  `https://virtserver.swaggerhub.com/fakenamespace/elderlings/1.0.0`


---

## 🏹 Endpoints

## 1. GET /characters/fitz

Retrieve detailed information about FitzChivalry Farseer.

### Description

Returns Fitz’s identity, titles, and magical bonds (Wit and Skill).

### Example Request

`GET /characters/fitz`

### Example Response

```
{
  "id": "fitz-001",
  "name": "FitzChivalry Farseer",
  "titles": ["Royal Bastard", "Catalyst", "Assassin"],
  "bonds": {
    "wit": ["Nighteyes"],
    "skill": ["Verity"]
  },
  "status": "Alive (mostly)"
}
```

---

## 2. GET /characters/nighteyes

Retrieve information about Nighteyes, Fitz’s Wit‑bonded wolf companion.

### Description

Returns species, personality traits, and bond information.

### Example Request

`GET /characters/nighteyes`

### Example Response

```
{
  "id": "wit-001",
  "name": "Nighteyes",
  "species": "Wolf",
  "bondedTo": "FitzChivalry Farseer",
  "traits": ["Loyal", "Sarcastic", "Wise"],
  "status": "Gone to the wolf-dream"
}
```

---

## 3. GET /assignments

List current and past assassin assignments.

### Description

Returns a collection of tasks handled by the royal assassin, including outcomes.

### Example Request

`GET /assignments`

### Example Response

```
{
  "assignments": [
    {
      "id": "task-001",
      "target": "Prince Regal",
      "status": "Failed (politics happened)"
    },
    {
      "id": "task-002",
      "target": "Forged Ones",
      "status": "Completed"
    }
  ]
}
```

---

## 🧪 Data Model Summary

### Character Object

|Field |Type	       |Description|
|------|-------------|-----------|
|id    |string       |Unique identifier|
|name  |string       |Character |
|titles|array[string]|Honorifics or roles|
|bonds |object	     |Wit and Skill connections|
|status|string	     |Current state|

### Assignment Object
|Field	|Type	 |Description  |
|-------|------|-------------|
|id	    |string|Assignment ID|
|target	|string|Intended target|
|status	|string|Outcome|

---

## 🐉 Core API Concepts
### REST

The API follows REST conventions: resources, predictable URLs, and standard HTTP methods.

### HTTP Methods
The API uses standard HTTP methods to interact with resources:

   |Method | Meaning|
   |-------|---------|
   | `GET` | retrieve data|
   | `POST`| create data|
   | `PUT` | update data|
   | `DELETE`| remove data|

### Response Format

All responses are JSON.

### Status Codes

   |Code |Description    |Meaning|
   |-----|----|-----------|
   |`200`|`OK` | successful request|
   |`404`|` Not Found` | resource does not exist|
   |`500`|` Internal Server Error` | unexpected server issue|

---

## 🗡 Technology Used

    - OpenAPI 3.0
    - Swagger Editor (local editing)
    - SwaggerHub Mock Server (auto‑generated)
    - JSON schema modeling
