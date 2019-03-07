---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Authentication Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Samii API Documentation! Used for developing standard API contract between front-end React, Node application and back-end machine learning, database applications.

We have language bindings in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/lord/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

<!-- ```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow` -->

<aside class="notice">
API will need to be validated using <code>API key</code>.
</aside>

# Questions

## Get list of profile questions

> The above command returns JSON structured like this:

```json
[
  {
    "question_id": "unique_question_identifier_A",
    "question_text": "Do you like this question?"
  },
  {
    "question_id": "unique_question_identifier_B",
    "question_text": "How about this question?"
  }
]
```

This endpoint retrieves all questions.

### HTTP Request

`GET http://<<samii_api_url>>.com/questions/all`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
-- | -- | -- 

<aside class="success">
Retrieving update version of profile questions to be performed by SQL query on the backend.
</aside>

## Submit response for student profile question

```json
{
  "student_id": 2,
  "question_id": "unique_question_identifier_A",
  "question_answer": 5
}
```

Endpoint submits a student response to a question.

### HTTP Request

`POST http://<<samii_api_url>>.com/questions/response`

API responds with score from data model if sufficient questions have been answered

OR

generic response awaiting further data gathering.

### API response

```json
{
  "student_id": 2,
  "sufficient": true,
  "profile_score": 1.7642
}
```

```json
{
  "student_id": 2,
  "sufficient": false,
  "profile_score": 0
}
```

<!-- ## Post answer to question

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete
 -->
