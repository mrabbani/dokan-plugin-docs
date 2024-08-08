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

## get__verification-requests

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/verification-requests', array(
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

r = requests.get('http://dokan-sample.test/verification-requests')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/verification-requests',
  params: {
  }

p JSON.parse(result)

```

`GET /verification-requests`

<h3 id="get__verification-requests-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|vendor_id|query|integer|false|Vendor ID associated with the verification request.|
|method_id|query|integer|false|Verification Method ID associated with the verification request.|
|status|query|string|false|The document type is enabled or not|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__verification-requests-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__verification-requests

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
    $response = $client->request('POST','http://dokan-sample.test/verification-requests', array(
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

r = requests.post('http://dokan-sample.test/verification-requests', params={
  'vendor_id': '0',  'method_id': '0',  'documents': [
  0
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

result = RestClient.post 'http://dokan-sample.test/verification-requests',
  params: {
  'vendor_id' => 'integer',
'method_id' => 'integer',
'documents' => 'array[integer]'
}, headers: headers

p JSON.parse(result)

```

`POST /verification-requests`

> Body parameter

```json
{
  "vendor_id": 0,
  "method_id": 0,
  "status": "string",
  "note": "string",
  "additional_info": {},
  "documents": [
    0
  ]
}
```

<h3 id="post__verification-requests-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vendor_id|query|integer|true|Vendor id associated with verification request.|
|method_id|query|integer|true|Verification Method id associated with verification request.|
|status|query|string|false|The verification request status.|
|note|query|string|false|The verification request note for administrator.|
|additional_info|query|object|false|The documents additional information.|
|documents|query|array[integer]|true|The documents for verification|
|body|body|object|true|none|
|» vendor_id|body|integer|false|Vendor id associated with verification request.|
|» method_id|body|integer|false|Verification Method id associated with verification request.|
|» status|body|string|false|The verification request status.|
|» note|body|string|false|The verification request note for administrator.|
|» additional_info|body|object|false|The documents additional information.|
|» documents|body|[integer]|false|The documents for verification|

<h3 id="post__verification-requests-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__verification-requests_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/verification-requests/{id}', array(
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

r = requests.get('http://dokan-sample.test/verification-requests/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/verification-requests/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /verification-requests/{id}`

<h3 id="get__verification-requests_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|none|

<h3 id="get__verification-requests_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__verification-requests_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/verification-requests/{id}', array(
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

r = requests.post('http://dokan-sample.test/verification-requests/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/verification-requests/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /verification-requests/{id}`

> Body parameter

```json
{
  "vendor_id": 0,
  "method_id": 0,
  "status": "string",
  "note": "string",
  "additional_info": {},
  "documents": [
    0
  ]
}
```

<h3 id="post__verification-requests_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vendor_id|query|integer|false|Vendor id associated with verification request.|
|method_id|query|integer|false|Verification Method id associated with verification request.|
|status|query|string|false|The verification request status.|
|note|query|string|false|The verification request note for administrator.|
|additional_info|query|object|false|The documents additional information.|
|documents|query|array[integer]|false|The documents for verification|
|body|body|object|true|none|
|» vendor_id|body|integer|false|Vendor id associated with verification request.|
|» method_id|body|integer|false|Verification Method id associated with verification request.|
|» status|body|string|false|The verification request status.|
|» note|body|string|false|The verification request note for administrator.|
|» additional_info|body|object|false|The documents additional information.|
|» documents|body|[integer]|false|The documents for verification|

<h3 id="post__verification-requests_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__verification-requests_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/verification-requests/{id}', array(
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

r = requests.put('http://dokan-sample.test/verification-requests/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/verification-requests/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /verification-requests/{id}`

> Body parameter

```json
{
  "vendor_id": 0,
  "method_id": 0,
  "status": "string",
  "note": "string",
  "additional_info": {},
  "documents": [
    0
  ]
}
```

<h3 id="put__verification-requests_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vendor_id|query|integer|false|Vendor id associated with verification request.|
|method_id|query|integer|false|Verification Method id associated with verification request.|
|status|query|string|false|The verification request status.|
|note|query|string|false|The verification request note for administrator.|
|additional_info|query|object|false|The documents additional information.|
|documents|query|array[integer]|false|The documents for verification|
|body|body|object|true|none|
|» vendor_id|body|integer|false|Vendor id associated with verification request.|
|» method_id|body|integer|false|Verification Method id associated with verification request.|
|» status|body|string|false|The verification request status.|
|» note|body|string|false|The verification request note for administrator.|
|» additional_info|body|object|false|The documents additional information.|
|» documents|body|[integer]|false|The documents for verification|

<h3 id="put__verification-requests_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__verification-requests_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/verification-requests/{id}', array(
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

r = requests.patch('http://dokan-sample.test/verification-requests/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/verification-requests/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /verification-requests/{id}`

> Body parameter

```json
{
  "vendor_id": 0,
  "method_id": 0,
  "status": "string",
  "note": "string",
  "additional_info": {},
  "documents": [
    0
  ]
}
```

<h3 id="patch__verification-requests_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vendor_id|query|integer|false|Vendor id associated with verification request.|
|method_id|query|integer|false|Verification Method id associated with verification request.|
|status|query|string|false|The verification request status.|
|note|query|string|false|The verification request note for administrator.|
|additional_info|query|object|false|The documents additional information.|
|documents|query|array[integer]|false|The documents for verification|
|body|body|object|true|none|
|» vendor_id|body|integer|false|Vendor id associated with verification request.|
|» method_id|body|integer|false|Verification Method id associated with verification request.|
|» status|body|string|false|The verification request status.|
|» note|body|string|false|The verification request note for administrator.|
|» additional_info|body|object|false|The documents additional information.|
|» documents|body|[integer]|false|The documents for verification|

<h3 id="patch__verification-requests_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__verification-requests_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/verification-requests/{id}', array(
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

r = requests.delete('http://dokan-sample.test/verification-requests/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/verification-requests/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /verification-requests/{id}`

<h3 id="delete__verification-requests_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|force|query|string|false|none|

<h3 id="delete__verification-requests_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

