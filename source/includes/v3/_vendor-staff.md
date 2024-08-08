---
title: null
language_tabs:
  - curl: CURL
  - php: PHP
  - python: Python
  - ruby: Ruby
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="">undefined vv1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="http://dokan-sample.test">http://dokan-sample.test</a>

<h1 id="-default">Default</h1>

## get__vendor-staff

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/vendor-staff', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests

r = requests.get('http://dokan-sample.test/vendor-staff')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/vendor-staff',
  params: {
  }

p JSON.parse(result)

```

`GET /vendor-staff`

<h3 id="get__vendor-staff-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|embed|
|context|edit|

<h3 id="get__vendor-staff-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__vendor-staff

> Code samples

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/vendor-staff', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('http://dokan-sample.test/vendor-staff', params={
  'email': 'user@example.com'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/vendor-staff',
  params: {
  'email' => 'string(email)'
}, headers: headers

p JSON.parse(result)

```

`POST /vendor-staff`

> Body parameter

```json
{
  "username": "string",
  "name": "string",
  "first_name": "string",
  "last_name": "string",
  "phone": "string",
  "email": "user@example.com",
  "nickname": "string",
  "password": "string"
}
```

<h3 id="post__vendor-staff-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|username|query|string|false|Login name for the user.|
|name|query|string|false|Display name for the user.|
|first_name|query|string|false|First name for the user.|
|last_name|query|string|false|Last name for the user.|
|phone|query|string|false|Phone number for the user.|
|email|query|string(email)|true|The email address for the user.|
|nickname|query|string|false|The nickname for the user.|
|password|query|string|false|Password for the user (never included).|
|body|body|object|true|none|
|» username|body|string|false|Login name for the user.|
|» name|body|string|false|Display name for the user.|
|» first_name|body|string|false|First name for the user.|
|» last_name|body|string|false|Last name for the user.|
|» phone|body|string|false|Phone number for the user.|
|» email|body|string(email)|false|The email address for the user.|
|» nickname|body|string|false|The nickname for the user.|
|» password|body|string|false|Password for the user (never included).|

<h3 id="post__vendor-staff-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__vendor-staff_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/vendor-staff/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests

r = requests.get('http://dokan-sample.test/vendor-staff/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/vendor-staff/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /vendor-staff/{id}`

<h3 id="get__vendor-staff_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|none|

<h3 id="get__vendor-staff_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__vendor-staff_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/vendor-staff/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('http://dokan-sample.test/vendor-staff/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/vendor-staff/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /vendor-staff/{id}`

> Body parameter

```json
{
  "username": "string",
  "name": "string",
  "first_name": "string",
  "last_name": "string",
  "phone": "string",
  "email": "user@example.com",
  "nickname": "string",
  "password": "string"
}
```

<h3 id="post__vendor-staff_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|username|query|string|false|Login name for the user.|
|name|query|string|false|Display name for the user.|
|first_name|query|string|false|First name for the user.|
|last_name|query|string|false|Last name for the user.|
|phone|query|string|false|Phone number for the user.|
|email|query|string(email)|false|The email address for the user.|
|nickname|query|string|false|The nickname for the user.|
|password|query|string|false|Password for the user (never included).|
|body|body|object|true|none|
|» username|body|string|false|Login name for the user.|
|» name|body|string|false|Display name for the user.|
|» first_name|body|string|false|First name for the user.|
|» last_name|body|string|false|Last name for the user.|
|» phone|body|string|false|Phone number for the user.|
|» email|body|string(email)|false|The email address for the user.|
|» nickname|body|string|false|The nickname for the user.|
|» password|body|string|false|Password for the user (never included).|

<h3 id="post__vendor-staff_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__vendor-staff_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/vendor-staff/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('http://dokan-sample.test/vendor-staff/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/vendor-staff/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /vendor-staff/{id}`

> Body parameter

```json
{
  "username": "string",
  "name": "string",
  "first_name": "string",
  "last_name": "string",
  "phone": "string",
  "email": "user@example.com",
  "nickname": "string",
  "password": "string"
}
```

<h3 id="put__vendor-staff_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|username|query|string|false|Login name for the user.|
|name|query|string|false|Display name for the user.|
|first_name|query|string|false|First name for the user.|
|last_name|query|string|false|Last name for the user.|
|phone|query|string|false|Phone number for the user.|
|email|query|string(email)|false|The email address for the user.|
|nickname|query|string|false|The nickname for the user.|
|password|query|string|false|Password for the user (never included).|
|body|body|object|true|none|
|» username|body|string|false|Login name for the user.|
|» name|body|string|false|Display name for the user.|
|» first_name|body|string|false|First name for the user.|
|» last_name|body|string|false|Last name for the user.|
|» phone|body|string|false|Phone number for the user.|
|» email|body|string(email)|false|The email address for the user.|
|» nickname|body|string|false|The nickname for the user.|
|» password|body|string|false|Password for the user (never included).|

<h3 id="put__vendor-staff_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__vendor-staff_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/vendor-staff/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.patch('http://dokan-sample.test/vendor-staff/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/vendor-staff/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /vendor-staff/{id}`

> Body parameter

```json
{
  "username": "string",
  "name": "string",
  "first_name": "string",
  "last_name": "string",
  "phone": "string",
  "email": "user@example.com",
  "nickname": "string",
  "password": "string"
}
```

<h3 id="patch__vendor-staff_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|username|query|string|false|Login name for the user.|
|name|query|string|false|Display name for the user.|
|first_name|query|string|false|First name for the user.|
|last_name|query|string|false|Last name for the user.|
|phone|query|string|false|Phone number for the user.|
|email|query|string(email)|false|The email address for the user.|
|nickname|query|string|false|The nickname for the user.|
|password|query|string|false|Password for the user (never included).|
|body|body|object|true|none|
|» username|body|string|false|Login name for the user.|
|» name|body|string|false|Display name for the user.|
|» first_name|body|string|false|First name for the user.|
|» last_name|body|string|false|Last name for the user.|
|» phone|body|string|false|Phone number for the user.|
|» email|body|string(email)|false|The email address for the user.|
|» nickname|body|string|false|The nickname for the user.|
|» password|body|string|false|Password for the user (never included).|

<h3 id="patch__vendor-staff_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__vendor-staff_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/vendor-staff/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests

r = requests.delete('http://dokan-sample.test/vendor-staff/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/vendor-staff/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /vendor-staff/{id}`

<h3 id="delete__vendor-staff_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|force|query|string|false|none|

<h3 id="delete__vendor-staff_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__vendor-staff_{id}_capabilities

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/vendor-staff/{id}/capabilities', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests

r = requests.get('http://dokan-sample.test/vendor-staff/{id}/capabilities')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/vendor-staff/{id}/capabilities',
  params: {
  }

p JSON.parse(result)

```

`GET /vendor-staff/{id}/capabilities`

<h3 id="get__vendor-staff_{id}_capabilities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__vendor-staff_{id}_capabilities

> Code samples

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/vendor-staff/{id}/capabilities', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('http://dokan-sample.test/vendor-staff/{id}/capabilities', params={
  'capabilities': [
  {
    "capability": "string",
    "access": true
  }
]
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/vendor-staff/{id}/capabilities',
  params: {
  'capabilities' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`POST /vendor-staff/{id}/capabilities`

> Body parameter

```json
{
  "capabilities": [
    {
      "capability": "string",
      "access": true
    }
  ]
}
```

<h3 id="post__vendor-staff_{id}_capabilities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|capabilities|query|array[object]|true|none|
|body|body|object|true|none|
|» capabilities|body|[object]|false|none|
|»» capability|body|string|true|Capability name|
|»» access|body|boolean|true|Has access to the  Capability|

<h3 id="post__vendor-staff_{id}_capabilities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__vendor-staff_{id}_capabilities

> Code samples

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/vendor-staff/{id}/capabilities', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('http://dokan-sample.test/vendor-staff/{id}/capabilities', params={
  'capabilities': [
  {
    "capability": "string",
    "access": true
  }
]
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/vendor-staff/{id}/capabilities',
  params: {
  'capabilities' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`PUT /vendor-staff/{id}/capabilities`

> Body parameter

```json
{
  "capabilities": [
    {
      "capability": "string",
      "access": true
    }
  ]
}
```

<h3 id="put__vendor-staff_{id}_capabilities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|capabilities|query|array[object]|true|none|
|body|body|object|true|none|
|» capabilities|body|[object]|false|none|
|»» capability|body|string|true|Capability name|
|»» access|body|boolean|true|Has access to the  Capability|

<h3 id="put__vendor-staff_{id}_capabilities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__vendor-staff_{id}_capabilities

> Code samples

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/vendor-staff/{id}/capabilities', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.patch('http://dokan-sample.test/vendor-staff/{id}/capabilities', params={
  'capabilities': [
  {
    "capability": "string",
    "access": true
  }
]
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/vendor-staff/{id}/capabilities',
  params: {
  'capabilities' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`PATCH /vendor-staff/{id}/capabilities`

> Body parameter

```json
{
  "capabilities": [
    {
      "capability": "string",
      "access": true
    }
  ]
}
```

<h3 id="patch__vendor-staff_{id}_capabilities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|capabilities|query|array[object]|true|none|
|body|body|object|true|none|
|» capabilities|body|[object]|false|none|
|»» capability|body|string|true|Capability name|
|»» access|body|boolean|true|Has access to the  Capability|

<h3 id="patch__vendor-staff_{id}_capabilities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__vendor-staff_capabilities

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/vendor-staff/capabilities', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```python
import requests

r = requests.get('http://dokan-sample.test/vendor-staff/capabilities')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/vendor-staff/capabilities',
  params: {
  }

p JSON.parse(result)

```

`GET /vendor-staff/capabilities`

<h3 id="get__vendor-staff_capabilities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

