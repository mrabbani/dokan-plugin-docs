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

## get__reverse-withdrawal_stores-balance

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/reverse-withdrawal/stores-balance', array(
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

r = requests.get('http://dokan-sample.test/reverse-withdrawal/stores-balance')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/reverse-withdrawal/stores-balance',
  params: {
  }

p JSON.parse(result)

```

`GET /reverse-withdrawal/stores-balance`

<h3 id="get__reverse-withdrawal_stores-balance-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|vendor_id|query|array[integer]|false|Vendor ID to filter form|
|trn_date|query|object|false|Get transactions via date range|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__reverse-withdrawal_stores-balance-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__reverse-withdrawal_vendor-due-status

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/reverse-withdrawal/vendor-due-status', array(
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

r = requests.get('http://dokan-sample.test/reverse-withdrawal/vendor-due-status')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/reverse-withdrawal/vendor-due-status',
  params: {
  }

p JSON.parse(result)

```

`GET /reverse-withdrawal/vendor-due-status`

<h3 id="get__reverse-withdrawal_vendor-due-status-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vendor_id|query|integer|false|Vendor ID to filter form|

<h3 id="get__reverse-withdrawal_vendor-due-status-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__reverse-withdrawal_transactions

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/reverse-withdrawal/transactions', array(
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

r = requests.get('http://dokan-sample.test/reverse-withdrawal/transactions', params={
  'vendor_id': '0',  'trn_date': {
  "from": "2019-08-24T14:15:22Z",
  "to": "2019-08-24T14:15:22Z"
}
})

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/reverse-withdrawal/transactions',
  params: {
  'vendor_id' => 'integer',
'trn_date' => 'object'
}

p JSON.parse(result)

```

`GET /reverse-withdrawal/transactions`

<h3 id="get__reverse-withdrawal_transactions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|vendor_id|query|integer|true|Vendor ID to filter form|
|trn_type|query|string|false|Transaction type to filter form|
|trn_date|query|object|true|Get transactions via date range|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|trn_type|opening_balance|
|trn_type|order_commission|
|trn_type|failed_transfer_reversal|
|trn_type|product_advertisement|
|trn_type|manual_order_commission|
|trn_type|vendor_payment|
|trn_type|order_refund|
|trn_type|manual_product|
|trn_type|manual_order|
|trn_type|other|

<h3 id="get__reverse-withdrawal_transactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__reverse-withdrawal_transactions

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
    $response = $client->request('POST','http://dokan-sample.test/reverse-withdrawal/transactions', array(
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

r = requests.post('http://dokan-sample.test/reverse-withdrawal/transactions', params={
  'trn_type': 'opening_balance',  'vendor_id': '0',  'note': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/reverse-withdrawal/transactions',
  params: {
  'trn_type' => 'string',
'vendor_id' => 'integer',
'note' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /reverse-withdrawal/transactions`

> Body parameter

```json
{
  "trn_id": 0,
  "trn_type": "opening_balance",
  "vendor_id": 0,
  "note": "string",
  "debit": "string",
  "credit": "string"
}
```

<h3 id="post__reverse-withdrawal_transactions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|trn_id|query|integer|false|Transaction ID|
|trn_type|query|string|true|Transaction type|
|vendor_id|query|integer|true|ID of the Store|
|note|query|string|true|Added note.|
|debit|query|string|false|Amount that site admin charged to store owner|
|credit|query|string|false|Amount that has been paid via store owner to site admin|
|body|body|object|true|none|
|» trn_id|body|integer|false|Transaction ID|
|» trn_type|body|string|false|Transaction type|
|» vendor_id|body|integer|false|ID of the Store|
|» note|body|string|false|Added note.|
|» debit|body|string|false|Amount that site admin charged to store owner|
|» credit|body|string|false|Amount that has been paid via store owner to site admin|

#### Enumerated Values

|Parameter|Value|
|---|---|
|trn_type|opening_balance|
|trn_type|order_commission|
|trn_type|failed_transfer_reversal|
|trn_type|product_advertisement|
|trn_type|manual_order_commission|
|trn_type|vendor_payment|
|trn_type|order_refund|
|trn_type|manual_product|
|trn_type|manual_order|
|trn_type|other|
|» trn_type|opening_balance|
|» trn_type|order_commission|
|» trn_type|failed_transfer_reversal|
|» trn_type|product_advertisement|
|» trn_type|manual_order_commission|
|» trn_type|vendor_payment|
|» trn_type|order_refund|
|» trn_type|manual_product|
|» trn_type|manual_order|
|» trn_type|other|

<h3 id="post__reverse-withdrawal_transactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__reverse-withdrawal_transaction-types

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/reverse-withdrawal/transaction-types', array(
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

r = requests.get('http://dokan-sample.test/reverse-withdrawal/transaction-types')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/reverse-withdrawal/transaction-types',
  params: {
  }

p JSON.parse(result)

```

`GET /reverse-withdrawal/transaction-types`

<h3 id="get__reverse-withdrawal_transaction-types-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__reverse-withdrawal_stores

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/reverse-withdrawal/stores', array(
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

r = requests.get('http://dokan-sample.test/reverse-withdrawal/stores')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/reverse-withdrawal/stores',
  params: {
  }

p JSON.parse(result)

```

`GET /reverse-withdrawal/stores`

<h3 id="get__reverse-withdrawal_stores-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__reverse-withdrawal_add-to-cart

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
    $response = $client->request('POST','http://dokan-sample.test/reverse-withdrawal/add-to-cart', array(
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

r = requests.post('http://dokan-sample.test/reverse-withdrawal/add-to-cart', params={
  'amount': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/reverse-withdrawal/add-to-cart',
  params: {
  'amount' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /reverse-withdrawal/add-to-cart`

> Body parameter

```json
{
  "amount": "string"
}
```

<h3 id="post__reverse-withdrawal_add-to-cart-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|amount|query|string|true|Payable amount|
|body|body|object|true|none|
|» amount|body|string|false|Payable amount|

<h3 id="post__reverse-withdrawal_add-to-cart-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

