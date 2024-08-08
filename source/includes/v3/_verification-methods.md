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

## get__verification-methods

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/verification-methods', array(
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

r = requests.get('http://dokan-sample.test/verification-methods')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/verification-methods',
  params: {
  }

p JSON.parse(result)

```

`GET /verification-methods`

<h3 id="get__verification-methods-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|required|query|boolean|false|The document type is required or not|
|status|query|boolean|false|The document type is enabled or not|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__verification-methods-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__verification-methods

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
    $response = $client->request('POST','http://dokan-sample.test/verification-methods', array(
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

r = requests.post('http://dokan-sample.test/verification-methods', params={
  'title': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/verification-methods',
  params: {
  'title' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /verification-methods`

> Body parameter

```json
{
  "title": "string",
  "help_text": "string",
  "status": true,
  "kind": "address",
  "required": true
}
```

<h3 id="post__verification-methods-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|title|query|string|true|Title of the resource.|
|help_text|query|string|false|Help Text of the resource.|
|status|query|boolean|false|The document type status is enabled or not|
|kind|query|string(text)|false|The document type kind|
|required|query|boolean|false|The document type is required or not|
|body|body|object|true|none|
|» title|body|string|false|Title of the resource.|
|» help_text|body|string|false|Help Text of the resource.|
|» status|body|boolean|false|The document type status is enabled or not|
|» kind|body|string(text)|false|The document type kind|
|» required|body|boolean|false|The document type is required or not|

#### Enumerated Values

|Parameter|Value|
|---|---|
|kind|address|
|kind|custom|
|» kind|address|
|» kind|custom|

<h3 id="post__verification-methods-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__verification-methods_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/verification-methods/{id}', array(
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

r = requests.get('http://dokan-sample.test/verification-methods/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/verification-methods/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /verification-methods/{id}`

<h3 id="get__verification-methods_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|none|

<h3 id="get__verification-methods_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__verification-methods_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/verification-methods/{id}', array(
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

r = requests.post('http://dokan-sample.test/verification-methods/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/verification-methods/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /verification-methods/{id}`

> Body parameter

```json
{
  "title": "string",
  "help_text": "string",
  "status": true,
  "kind": "address",
  "required": true
}
```

<h3 id="post__verification-methods_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|title|query|string|false|Title of the resource.|
|help_text|query|string|false|Help Text of the resource.|
|status|query|boolean|false|The document type status is enabled or not|
|kind|query|string(text)|false|The document type kind|
|required|query|boolean|false|The document type is required or not|
|body|body|object|true|none|
|» title|body|string|false|Title of the resource.|
|» help_text|body|string|false|Help Text of the resource.|
|» status|body|boolean|false|The document type status is enabled or not|
|» kind|body|string(text)|false|The document type kind|
|» required|body|boolean|false|The document type is required or not|

#### Enumerated Values

|Parameter|Value|
|---|---|
|kind|address|
|kind|custom|
|» kind|address|
|» kind|custom|

<h3 id="post__verification-methods_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__verification-methods_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/verification-methods/{id}', array(
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

r = requests.put('http://dokan-sample.test/verification-methods/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/verification-methods/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /verification-methods/{id}`

> Body parameter

```json
{
  "title": "string",
  "help_text": "string",
  "status": true,
  "kind": "address",
  "required": true
}
```

<h3 id="put__verification-methods_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|title|query|string|false|Title of the resource.|
|help_text|query|string|false|Help Text of the resource.|
|status|query|boolean|false|The document type status is enabled or not|
|kind|query|string(text)|false|The document type kind|
|required|query|boolean|false|The document type is required or not|
|body|body|object|true|none|
|» title|body|string|false|Title of the resource.|
|» help_text|body|string|false|Help Text of the resource.|
|» status|body|boolean|false|The document type status is enabled or not|
|» kind|body|string(text)|false|The document type kind|
|» required|body|boolean|false|The document type is required or not|

#### Enumerated Values

|Parameter|Value|
|---|---|
|kind|address|
|kind|custom|
|» kind|address|
|» kind|custom|

<h3 id="put__verification-methods_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__verification-methods_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/verification-methods/{id}', array(
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

r = requests.patch('http://dokan-sample.test/verification-methods/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/verification-methods/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /verification-methods/{id}`

> Body parameter

```json
{
  "title": "string",
  "help_text": "string",
  "status": true,
  "kind": "address",
  "required": true
}
```

<h3 id="patch__verification-methods_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|title|query|string|false|Title of the resource.|
|help_text|query|string|false|Help Text of the resource.|
|status|query|boolean|false|The document type status is enabled or not|
|kind|query|string(text)|false|The document type kind|
|required|query|boolean|false|The document type is required or not|
|body|body|object|true|none|
|» title|body|string|false|Title of the resource.|
|» help_text|body|string|false|Help Text of the resource.|
|» status|body|boolean|false|The document type status is enabled or not|
|» kind|body|string(text)|false|The document type kind|
|» required|body|boolean|false|The document type is required or not|

#### Enumerated Values

|Parameter|Value|
|---|---|
|kind|address|
|kind|custom|
|» kind|address|
|» kind|custom|

<h3 id="patch__verification-methods_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__verification-methods_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/verification-methods/{id}', array(
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

r = requests.delete('http://dokan-sample.test/verification-methods/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/verification-methods/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /verification-methods/{id}`

<h3 id="delete__verification-methods_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|force|query|string|false|none|

<h3 id="delete__verification-methods_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

