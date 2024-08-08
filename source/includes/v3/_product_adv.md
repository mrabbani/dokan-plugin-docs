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

## get__product_adv

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/product_adv', array(
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

r = requests.get('http://dokan-sample.test/product_adv')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/product_adv',
  params: {
  }

p JSON.parse(result)

```

`GET /product_adv`

<h3 id="get__product_adv-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|vendor_id|query|array[integer]|false|Vendor IDs to filter form|
|product_id|query|array[integer]|false|Product IDs to filter form|
|order_id|query|array[integer]|false|Order IDs to filter form|
|status|query|integer|false|Advertised product status, 0 to get all status, 1 for active advertisements and 2 for inactive advertisements|
|expires_at|query|object|false|Get advertised products by their expire date|
|created_via|query|string|false|Filter how advertisement was created|
|return|query|string|false|How data will be returned|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|status|0|
|status|1|
|status|2|
|created_via||
|created_via|order|
|created_via|admin|
|created_via|subscription|
|created_via|free|
|return|all|
|return|ids|
|return|count|
|return|individual_count|

<h3 id="get__product_adv-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__product_adv_{id}_expire

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/product_adv/{id}/expire', array(
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

r = requests.post('http://dokan-sample.test/product_adv/{id}/expire')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/product_adv/{id}/expire',
  params: {
  }

p JSON.parse(result)

```

`POST /product_adv/{id}/expire`

<h3 id="post__product_adv_{id}_expire-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="post__product_adv_{id}_expire-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__product_adv_{id}_expire

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/product_adv/{id}/expire', array(
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

r = requests.put('http://dokan-sample.test/product_adv/{id}/expire')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/product_adv/{id}/expire',
  params: {
  }

p JSON.parse(result)

```

`PUT /product_adv/{id}/expire`

<h3 id="put__product_adv_{id}_expire-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="put__product_adv_{id}_expire-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__product_adv_{id}_expire

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/product_adv/{id}/expire', array(
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

r = requests.patch('http://dokan-sample.test/product_adv/{id}/expire')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/product_adv/{id}/expire',
  params: {
  }

p JSON.parse(result)

```

`PATCH /product_adv/{id}/expire`

<h3 id="patch__product_adv_{id}_expire-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="patch__product_adv_{id}_expire-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__product_adv_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/product_adv/{id}', array(
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

r = requests.delete('http://dokan-sample.test/product_adv/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/product_adv/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /product_adv/{id}`

<h3 id="delete__product_adv_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="delete__product_adv_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__product_adv_batch

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
    $response = $client->request('POST','http://dokan-sample.test/product_adv/batch', array(
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

r = requests.post('http://dokan-sample.test/product_adv/batch', params={
  'action': 'expire',  'ids': [
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

result = RestClient.post 'http://dokan-sample.test/product_adv/batch',
  params: {
  'action' => 'string',
'ids' => 'array[integer]'
}, headers: headers

p JSON.parse(result)

```

`POST /product_adv/batch`

> Body parameter

```json
{
  "context": "view",
  "action": "expire",
  "ids": [
    0
  ]
}
```

<h3 id="post__product_adv_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|action|query|string|true|Batch action name to process|
|ids|query|array[integer]|true|Batch action to carry on advertisement items|
|body|body|object|true|none|
|» context|body|string|false|Scope under which the request is made; determines fields present in response.|
|» action|body|string|false|Batch action name to process|
|» ids|body|[integer]|false|Batch action to carry on advertisement items|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|action|expire|
|action|delete|
|» context|view|
|» context|edit|
|» action|expire|
|» action|delete|

<h3 id="post__product_adv_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__product_adv_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/product_adv/batch', array(
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

r = requests.put('http://dokan-sample.test/product_adv/batch', params={
  'action': 'expire',  'ids': [
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

result = RestClient.put 'http://dokan-sample.test/product_adv/batch',
  params: {
  'action' => 'string',
'ids' => 'array[integer]'
}, headers: headers

p JSON.parse(result)

```

`PUT /product_adv/batch`

> Body parameter

```json
{
  "context": "view",
  "action": "expire",
  "ids": [
    0
  ]
}
```

<h3 id="put__product_adv_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|action|query|string|true|Batch action name to process|
|ids|query|array[integer]|true|Batch action to carry on advertisement items|
|body|body|object|true|none|
|» context|body|string|false|Scope under which the request is made; determines fields present in response.|
|» action|body|string|false|Batch action name to process|
|» ids|body|[integer]|false|Batch action to carry on advertisement items|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|action|expire|
|action|delete|
|» context|view|
|» context|edit|
|» action|expire|
|» action|delete|

<h3 id="put__product_adv_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__product_adv_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/product_adv/batch', array(
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

r = requests.patch('http://dokan-sample.test/product_adv/batch', params={
  'action': 'expire',  'ids': [
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

result = RestClient.patch 'http://dokan-sample.test/product_adv/batch',
  params: {
  'action' => 'string',
'ids' => 'array[integer]'
}, headers: headers

p JSON.parse(result)

```

`PATCH /product_adv/batch`

> Body parameter

```json
{
  "context": "view",
  "action": "expire",
  "ids": [
    0
  ]
}
```

<h3 id="patch__product_adv_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|action|query|string|true|Batch action name to process|
|ids|query|array[integer]|true|Batch action to carry on advertisement items|
|body|body|object|true|none|
|» context|body|string|false|Scope under which the request is made; determines fields present in response.|
|» action|body|string|false|Batch action name to process|
|» ids|body|[integer]|false|Batch action to carry on advertisement items|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|action|expire|
|action|delete|
|» context|view|
|» context|edit|
|» action|expire|
|» action|delete|

<h3 id="patch__product_adv_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__product_adv_stores

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/product_adv/stores', array(
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

r = requests.get('http://dokan-sample.test/product_adv/stores')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/product_adv/stores',
  params: {
  }

p JSON.parse(result)

```

`GET /product_adv/stores`

<h3 id="get__product_adv_stores-parameters">Parameters</h3>

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
|context|edit|

<h3 id="get__product_adv_stores-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__product_adv_create

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
    $response = $client->request('POST','http://dokan-sample.test/product_adv/create', array(
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

r = requests.post('http://dokan-sample.test/product_adv/create', params={
  'product_id': '0',  'vendor_id': '0'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/product_adv/create',
  params: {
  'product_id' => 'integer',
'vendor_id' => 'integer'
}, headers: headers

p JSON.parse(result)

```

`POST /product_adv/create`

> Body parameter

```json
{
  "product_id": 0,
  "vendor_id": 0,
  "reverse_withdrawal_entry": true
}
```

<h3 id="post__product_adv_create-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|query|integer|true|To be advertise product id.|
|vendor_id|query|integer|true|Vendor of the product.|
|reverse_withdrawal_entry|query|boolean|false|Add Reverse Withdrawal Entry.|
|body|body|object|true|none|
|» product_id|body|integer|false|To be advertise product id.|
|» vendor_id|body|integer|false|Vendor of the product.|
|» reverse_withdrawal_entry|body|boolean|false|Add Reverse Withdrawal Entry.|

<h3 id="post__product_adv_create-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

