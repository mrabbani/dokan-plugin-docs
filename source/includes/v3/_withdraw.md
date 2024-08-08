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

## get__withdraw

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/withdraw', array(
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

r = requests.get('http://dokan-sample.test/withdraw')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/withdraw',
  params: {
  }

p JSON.parse(result)

```

`GET /withdraw`

<h3 id="get__withdraw-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|ids|query|array[integer]|false|IDs of withdraws|
|is_export|query|boolean|false|Is withdraws exportable|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__withdraw-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__withdraw

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
    $response = $client->request('POST','http://dokan-sample.test/withdraw', array(
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

r = requests.post('http://dokan-sample.test/withdraw', params={
  'amount': 'string',  'method': 'paypal'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/withdraw',
  params: {
  'amount' => 'string',
'method' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /withdraw`

> Body parameter

```json
{
  "user_id": 0,
  "amount": "string",
  "status": "pending",
  "method": "paypal",
  "note": "string"
}
```

<h3 id="post__withdraw-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|user_id|query|integer|false|Requested User ID|
|amount|query|string|true|The amount of discount. Should always be numeric, even if setting a percentage.|
|status|query|string|false|Withdraw status|
|method|query|string|true|Withdraw Method|
|note|query|string|false|Withdraw Notes|
|body|body|object|true|none|
|» user_id|body|integer|false|Requested User ID|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» status|body|string|false|Withdraw status|
|» method|body|string|false|Withdraw Method|
|» note|body|string|false|Withdraw Notes|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|pending|
|status|approved|
|status|cancelled|
|method|paypal|
|method|bank|
|method|dokan-stripe-connect|
|» status|pending|
|» status|approved|
|» status|cancelled|
|» method|paypal|
|» method|bank|
|» method|dokan-stripe-connect|

<h3 id="post__withdraw-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__withdraw_balance

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/withdraw/balance', array(
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

r = requests.get('http://dokan-sample.test/withdraw/balance')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/withdraw/balance',
  params: {
  }

p JSON.parse(result)

```

`GET /withdraw/balance`

<h3 id="get__withdraw_balance-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__withdraw_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/withdraw/{id}', array(
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

r = requests.get('http://dokan-sample.test/withdraw/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/withdraw/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /withdraw/{id}`

<h3 id="get__withdraw_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="get__withdraw_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__withdraw_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/withdraw/{id}', array(
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

r = requests.post('http://dokan-sample.test/withdraw/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/withdraw/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /withdraw/{id}`

> Body parameter

```json
{
  "user_id": 0,
  "amount": "string",
  "status": "pending",
  "method": "paypal",
  "note": "string"
}
```

<h3 id="post__withdraw_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|user_id|query|integer|false|Requested User ID|
|amount|query|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|status|query|string|false|Withdraw status|
|method|query|string|false|Withdraw Method|
|note|query|string|false|Withdraw Notes|
|body|body|object|true|none|
|» user_id|body|integer|false|Requested User ID|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» status|body|string|false|Withdraw status|
|» method|body|string|false|Withdraw Method|
|» note|body|string|false|Withdraw Notes|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|pending|
|status|approved|
|status|cancelled|
|method|paypal|
|method|bank|
|method|dokan-stripe-connect|
|» status|pending|
|» status|approved|
|» status|cancelled|
|» method|paypal|
|» method|bank|
|» method|dokan-stripe-connect|

<h3 id="post__withdraw_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__withdraw_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/withdraw/{id}', array(
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

r = requests.put('http://dokan-sample.test/withdraw/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/withdraw/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /withdraw/{id}`

> Body parameter

```json
{
  "user_id": 0,
  "amount": "string",
  "status": "pending",
  "method": "paypal",
  "note": "string"
}
```

<h3 id="put__withdraw_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|user_id|query|integer|false|Requested User ID|
|amount|query|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|status|query|string|false|Withdraw status|
|method|query|string|false|Withdraw Method|
|note|query|string|false|Withdraw Notes|
|body|body|object|true|none|
|» user_id|body|integer|false|Requested User ID|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» status|body|string|false|Withdraw status|
|» method|body|string|false|Withdraw Method|
|» note|body|string|false|Withdraw Notes|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|pending|
|status|approved|
|status|cancelled|
|method|paypal|
|method|bank|
|method|dokan-stripe-connect|
|» status|pending|
|» status|approved|
|» status|cancelled|
|» method|paypal|
|» method|bank|
|» method|dokan-stripe-connect|

<h3 id="put__withdraw_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__withdraw_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/withdraw/{id}', array(
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

r = requests.patch('http://dokan-sample.test/withdraw/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/withdraw/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /withdraw/{id}`

> Body parameter

```json
{
  "user_id": 0,
  "amount": "string",
  "status": "pending",
  "method": "paypal",
  "note": "string"
}
```

<h3 id="patch__withdraw_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|user_id|query|integer|false|Requested User ID|
|amount|query|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|status|query|string|false|Withdraw status|
|method|query|string|false|Withdraw Method|
|note|query|string|false|Withdraw Notes|
|body|body|object|true|none|
|» user_id|body|integer|false|Requested User ID|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» status|body|string|false|Withdraw status|
|» method|body|string|false|Withdraw Method|
|» note|body|string|false|Withdraw Notes|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|pending|
|status|approved|
|status|cancelled|
|method|paypal|
|method|bank|
|method|dokan-stripe-connect|
|» status|pending|
|» status|approved|
|» status|cancelled|
|» method|paypal|
|» method|bank|
|» method|dokan-stripe-connect|

<h3 id="patch__withdraw_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__withdraw_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/withdraw/{id}', array(
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

r = requests.delete('http://dokan-sample.test/withdraw/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/withdraw/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /withdraw/{id}`

<h3 id="delete__withdraw_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="delete__withdraw_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__withdraw_payment_methods

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/withdraw/payment_methods', array(
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

r = requests.get('http://dokan-sample.test/withdraw/payment_methods')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/withdraw/payment_methods',
  params: {
  }

p JSON.parse(result)

```

`GET /withdraw/payment_methods`

<h3 id="get__withdraw_payment_methods-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__withdraw_batch

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
    $response = $client->request('POST','http://dokan-sample.test/withdraw/batch', array(
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

r = requests.post('http://dokan-sample.test/withdraw/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/withdraw/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /withdraw/batch`

> Body parameter

```json
{
  "approved": [
    0
  ],
  "cancelled": [
    0
  ],
  "delete": [
    0
  ]
}
```

<h3 id="post__withdraw_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|approved|query|array[integer]|false|List of withdraw IDs to be approved|
|cancelled|query|array[integer]|false|List of withdraw IDs to be cancelled|
|delete|query|array[integer]|false|List of withdraw IDs to be deleted|
|body|body|object|true|none|
|» approved|body|[integer]|false|List of withdraw IDs to be approved|
|» cancelled|body|[integer]|false|List of withdraw IDs to be cancelled|
|» delete|body|[integer]|false|List of withdraw IDs to be deleted|

<h3 id="post__withdraw_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__withdraw_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/withdraw/batch', array(
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

r = requests.put('http://dokan-sample.test/withdraw/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/withdraw/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /withdraw/batch`

> Body parameter

```json
{
  "approved": [
    0
  ],
  "cancelled": [
    0
  ],
  "delete": [
    0
  ]
}
```

<h3 id="put__withdraw_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|approved|query|array[integer]|false|List of withdraw IDs to be approved|
|cancelled|query|array[integer]|false|List of withdraw IDs to be cancelled|
|delete|query|array[integer]|false|List of withdraw IDs to be deleted|
|body|body|object|true|none|
|» approved|body|[integer]|false|List of withdraw IDs to be approved|
|» cancelled|body|[integer]|false|List of withdraw IDs to be cancelled|
|» delete|body|[integer]|false|List of withdraw IDs to be deleted|

<h3 id="put__withdraw_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__withdraw_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/withdraw/batch', array(
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

r = requests.patch('http://dokan-sample.test/withdraw/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/withdraw/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /withdraw/batch`

> Body parameter

```json
{
  "approved": [
    0
  ],
  "cancelled": [
    0
  ],
  "delete": [
    0
  ]
}
```

<h3 id="patch__withdraw_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|approved|query|array[integer]|false|List of withdraw IDs to be approved|
|cancelled|query|array[integer]|false|List of withdraw IDs to be cancelled|
|delete|query|array[integer]|false|List of withdraw IDs to be deleted|
|body|body|object|true|none|
|» approved|body|[integer]|false|List of withdraw IDs to be approved|
|» cancelled|body|[integer]|false|List of withdraw IDs to be cancelled|
|» delete|body|[integer]|false|List of withdraw IDs to be deleted|

<h3 id="patch__withdraw_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__withdraw_charges

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/withdraw/charges', array(
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

r = requests.get('http://dokan-sample.test/withdraw/charges')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/withdraw/charges',
  params: {
  }

p JSON.parse(result)

```

`GET /withdraw/charges`

<h3 id="get__withdraw_charges-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__withdraw_charge

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/withdraw/charge', array(
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

r = requests.get('http://dokan-sample.test/withdraw/charge', params={
  'method': 'paypal',  'amount': '0'
})

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/withdraw/charge',
  params: {
  'method' => 'string',
'amount' => 'number'
}

p JSON.parse(result)

```

`GET /withdraw/charge`

<h3 id="get__withdraw_charge-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|method|query|string|true|Withdraw method key|
|amount|query|number|true|Withdraw amount|

#### Enumerated Values

|Parameter|Value|
|---|---|
|method|paypal|
|method|bank|
|method|dokan-stripe-connect|

<h3 id="get__withdraw_charge-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

