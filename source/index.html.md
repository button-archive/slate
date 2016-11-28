---
title: API Reference

language_tabs:
  - objective_c
  - swift
  - java
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```objective_c
Tyler *tyler = [Tyler apiUser:@"username" apiKey:@"password"];
```

```swift
let session = Session()
session.authentication = Authentication.apiKey("SG.abcdefghijklmnop.qrstuvwxyz012345-6789")

/*
`Session` also has a singleton instance that you can configure once and reuse throughout your code.
*/
Session.shared.authentication = Authentication.apiKey("SG.abcdefghijklmnop.qrstuvwxyz012345-6789")
```

```java
@Override
protected Void doInBackground(Void... params) {

  try {
    tyler tyler = new tyler(tyler_USERNAME, tyler_PASSWORD);

    tyler.Email email = new tyler.Email();

    // Get values from edit text to compose email
    // TODO: Validate edit texts
    email.addTo(mTo);
    email.setFrom(mFrom);
    email.setSubject(mSubject);
    email.setText(mText);

    // Attach image
    if (mUri != null) {
      email.addAttachment(mAttachmentName, mAppContext.getContentResolver().openInputStream(mUri));
    }

    // Send email, execute http request
    tyler.Response response = tyler.send(email);
    mMsgResponse = response.getMessage();

    Log.d("SendAppExample", mMsgResponse);

  } catch (tylerException | IOException e) {
    Log.e("SendAppExample", e.toString());
  }

  return null;
}
```

```ruby
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

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Kittens

## Get All Kittens

```objective_c
h = 2;
```

```swift
let session = Session()
session.authentication = Authentication.apiKey("SG.abcdefghijklmnop.qrstuvwxyz012345-6789")

/*
`Session` also has a singleton instance that you can configure once and reuse throughout your code.
*/
Session.shared.authentication = Authentication.apiKey("SG.abcdefghijklmnop.qrstuvwxyz012345-6789")
```

```java
@Override
protected Void doInBackground(Void... params) {

  try {
    tyler tyler = new tyler(tyler_USERNAME, tyler_PASSWORD);

    tyler.Email email = new tyler.Email();

    // Get values from edit text to compose email
    // TODO: Validate edit texts
    email.addTo(mTo);
    email.setFrom(mFrom);
    email.setSubject(mSubject);
    email.setText(mText);

    // Attach image
    if (mUri != null) {
      email.addAttachment(mAttachmentName, mAppContext.getContentResolver().openInputStream(mUri));
    }

    // Send email, execute http request
    tyler.Response response = tyler.send(email);
    mMsgResponse = response.getMessage();

    Log.d("SendAppExample", mMsgResponse);

  } catch (tylerException | IOException e) {
    Log.e("SendAppExample", e.toString());
  }

  return null;
}
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```objective_c
h = 2;
```

```swift
let session = Session()
session.authentication = Authentication.apiKey("SG.abcdefghijklmnop.qrstuvwxyz012345-6789")

/*
`Session` also has a singleton instance that you can configure once and reuse throughout your code.
*/
Session.shared.authentication = Authentication.apiKey("SG.abcdefghijklmnop.qrstuvwxyz012345-6789")
```

```java
@Override
protected Void doInBackground(Void... params) {

  try {
    tyler tyler = new tyler(tyler_USERNAME, tyler_PASSWORD);

    tyler.Email email = new tyler.Email();

    // Get values from edit text to compose email
    // TODO: Validate edit texts
    email.addTo(mTo);
    email.setFrom(mFrom);
    email.setSubject(mSubject);
    email.setText(mText);

    // Attach image
    if (mUri != null) {
      email.addAttachment(mAttachmentName, mAppContext.getContentResolver().openInputStream(mUri));
    }

    // Send email, execute http request
    tyler.Response response = tyler.send(email);
    mMsgResponse = response.getMessage();

    Log.d("SendAppExample", mMsgResponse);

  } catch (tylerException | IOException e) {
    Log.e("SendAppExample", e.toString());
  }

  return null;
}
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve
