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

## get__orders

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/orders', array(
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

r = requests.get('http://dokan-sample.test/orders')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/orders',
  params: {
  }

p JSON.parse(result)

```

`GET /orders`

<h3 id="get__orders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Order id to search order|
|seller_id|query|integer|false|Orders belongs to specific seller|
|status|query|string|false|Order status.|
|date_created|query|string(date-time)|false|The date the order was created, in the site's timezone.|
|customer_id|query|string|false|User ID who owns the order. 0 for guests.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__orders_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/orders/{id}', array(
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

r = requests.get('http://dokan-sample.test/orders/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/orders/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /orders/{id}`

<h3 id="get__orders_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Order id to search order|
|seller_id|query|integer|false|Orders belongs to specific seller|
|status|query|string|false|Order status.|
|date_created|query|string(date-time)|false|The date the order was created, in the site's timezone.|
|customer_id|query|string|false|User ID who owns the order. 0 for guests.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__orders_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__orders_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/orders/{id}', array(
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

r = requests.post('http://dokan-sample.test/orders/{id}', params={
  'status': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/orders/{id}',
  params: {
  'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /orders/{id}`

> Body parameter

```json
{
  "status": "string"
}
```

<h3 id="post__orders_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|status|query|string|true|Order Status|
|body|body|object|true|none|
|» status|body|string|false|Order Status|

<h3 id="post__orders_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__orders_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/orders/{id}', array(
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

r = requests.put('http://dokan-sample.test/orders/{id}', params={
  'status': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/orders/{id}',
  params: {
  'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`PUT /orders/{id}`

> Body parameter

```json
{
  "status": "string"
}
```

<h3 id="put__orders_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|status|query|string|true|Order Status|
|body|body|object|true|none|
|» status|body|string|false|Order Status|

<h3 id="put__orders_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__orders_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/orders/{id}', array(
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

r = requests.patch('http://dokan-sample.test/orders/{id}', params={
  'status': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/orders/{id}',
  params: {
  'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`PATCH /orders/{id}`

> Body parameter

```json
{
  "status": "string"
}
```

<h3 id="patch__orders_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|status|query|string|true|Order Status|
|body|body|object|true|none|
|» status|body|string|false|Order Status|

<h3 id="patch__orders_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__orders_{id}_notes

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/orders/{id}/notes', array(
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

r = requests.get('http://dokan-sample.test/orders/{id}/notes')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/orders/{id}/notes',
  params: {
  }

p JSON.parse(result)

```

`GET /orders/{id}/notes`

<h3 id="get__orders_{id}_notes-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Order id to search order|
|seller_id|query|integer|false|Orders belongs to specific seller|
|status|query|string|false|Order status.|
|date_created|query|string(date-time)|false|The date the order was created, in the site's timezone.|
|customer_id|query|string|false|User ID who owns the order. 0 for guests.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__orders_{id}_notes-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__orders_{id}_notes

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
    $response = $client->request('POST','http://dokan-sample.test/orders/{id}/notes', array(
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

r = requests.post('http://dokan-sample.test/orders/{id}/notes', params={
  'note': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/orders/{id}/notes',
  params: {
  'note' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /orders/{id}/notes`

> Body parameter

```json
{
  "parent_id": 0,
  "seller_id": 0,
  "status": "pending",
  "currency": "AED",
  "customer_id": "string",
  "search": "string",
  "customer_note": "string",
  "billing": {
    "first_name": "string",
    "last_name": "string",
    "company": "string",
    "address_1": "string",
    "address_2": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string",
    "email": "user@example.com",
    "phone": "string"
  },
  "shipping": {
    "first_name": "string",
    "last_name": "string",
    "company": "string",
    "address_1": "string",
    "address_2": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "payment_method": "string",
  "payment_method_title": "string",
  "transaction_id": "string",
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ],
  "line_items": [
    {
      "id": 0,
      "name": "string",
      "product_id": "string",
      "variation_id": 0,
      "quantity": 0,
      "tax_class": "string",
      "subtotal": "string",
      "subtotal_tax": "string",
      "total": "string",
      "total_tax": "string",
      "taxes": [
        {
          "id": 0,
          "total": "string",
          "subtotal": "string"
        }
      ],
      "meta_data": [
        {
          "id": 0,
          "key": "string",
          "value": "string"
        }
      ],
      "sku": "string",
      "price": 0
    }
  ],
  "shipping_lines": [
    {
      "id": 0,
      "method_title": "string",
      "method_id": "string",
      "total": "string",
      "total_tax": "string",
      "taxes": [
        {
          "id": 0,
          "total": "string"
        }
      ],
      "meta_data": [
        {
          "id": 0,
          "key": "string",
          "value": "string"
        }
      ]
    }
  ],
  "fee_lines": [
    {
      "id": 0,
      "name": "string",
      "tax_class": "string",
      "tax_status": "taxable",
      "total": "string",
      "total_tax": "string",
      "taxes": [
        {
          "id": 0,
          "total": "string",
          "subtotal": "string"
        }
      ],
      "meta_data": [
        {
          "id": 0,
          "key": "string",
          "value": "string"
        }
      ]
    }
  ],
  "coupon_lines": [
    {
      "id": 0,
      "code": "string",
      "discount": "string",
      "discount_tax": "string",
      "meta_data": [
        {
          "id": 0,
          "key": "string",
          "value": "string"
        }
      ]
    }
  ],
  "set_paid": true,
  "note": "string"
}
```

<h3 id="post__orders_{id}_notes-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|parent_id|query|integer|false|Parent order ID.|
|seller_id|query|integer|false|Orders belongs to specific seller|
|status|query|string|false|Order status.|
|currency|query|string|false|Currency the order was created with, in ISO format.|
|customer_id|query|string|false|User ID who owns the order. 0 for guests.|
|search|query|string|false|Order id to search order|
|customer_note|query|string|false|Note left by customer during checkout.|
|billing|query|object|false|Billing address.|
|shipping|query|object|false|Shipping address.|
|payment_method|query|string|false|Payment method ID.|
|payment_method_title|query|string|false|Payment method title.|
|transaction_id|query|string|false|Unique transaction ID.|
|meta_data|query|array[object]|false|Meta data.|
|line_items|query|array[object]|false|Line items data.|
|shipping_lines|query|array[object]|false|Shipping lines data.|
|fee_lines|query|array[object]|false|Fee lines data.|
|coupon_lines|query|array[object]|false|Coupons line data.|
|set_paid|query|boolean|false|Define if the order is paid. It will set the status to processing and reduce stock items.|
|note|query|string|true|Order note content.|
|body|body|object|true|none|
|» parent_id|body|integer|false|Parent order ID.|
|» seller_id|body|integer|false|Orders belongs to specific seller|
|» status|body|string|false|Order status.|
|» currency|body|string|false|Currency the order was created with, in ISO format.|
|» customer_id|body|string|false|User ID who owns the order. 0 for guests.|
|» search|body|string|false|Order id to search order|
|» customer_note|body|string|false|Note left by customer during checkout.|
|» billing|body|object|false|Billing address.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|Country code in ISO 3166-1 alpha-2 format.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|Shipping address.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|Country code in ISO 3166-1 alpha-2 format.|
|» payment_method|body|string|false|Payment method ID.|
|» payment_method_title|body|string|false|Payment method title.|
|» transaction_id|body|string|false|Unique transaction ID.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|
|» line_items|body|[object]|false|Line items data.|
|»» id|body|integer|false|Item ID.|
|»» name|body|string|false|Product name.|
|»» product_id|body|string|false|Product ID.|
|»» variation_id|body|integer|false|Variation ID, if applicable.|
|»» quantity|body|integer|false|Quantity ordered.|
|»» tax_class|body|string|false|Tax class of product.|
|»» subtotal|body|string|false|Line subtotal (before discounts).|
|»» subtotal_tax|body|string|false|Line subtotal tax (before discounts).|
|»» total|body|string|false|Line total (after discounts).|
|»» total_tax|body|string|false|Line total tax (after discounts).|
|»» taxes|body|[object]|false|Line taxes.|
|»»» id|body|integer|false|Tax rate ID.|
|»»» total|body|string|false|Tax total.|
|»»» subtotal|body|string|false|Tax subtotal.|
|»» meta_data|body|[object]|false|Meta data.|
|»»» id|body|integer|false|Meta ID.|
|»»» key|body|string|false|Meta key.|
|»»» value|body|string|false|Meta value.|
|»» sku|body|string|false|Product SKU.|
|»» price|body|number|false|Product price.|
|» shipping_lines|body|[object]|false|Shipping lines data.|
|»» id|body|integer|false|Item ID.|
|»» method_title|body|string|false|Shipping method name.|
|»» method_id|body|string|false|Shipping method ID.|
|»» total|body|string|false|Line total (after discounts).|
|»» total_tax|body|string|false|Line total tax (after discounts).|
|»» taxes|body|[object]|false|Line taxes.|
|»»» id|body|integer|false|Tax rate ID.|
|»»» total|body|string|false|Tax total.|
|»» meta_data|body|[object]|false|Meta data.|
|»»» id|body|integer|false|Meta ID.|
|»»» key|body|string|false|Meta key.|
|»»» value|body|string|false|Meta value.|
|» fee_lines|body|[object]|false|Fee lines data.|
|»» id|body|integer|false|Item ID.|
|»» name|body|string|false|Fee name.|
|»» tax_class|body|string|false|Tax class of fee.|
|»» tax_status|body|string|false|Tax status of fee.|
|»» total|body|string|false|Line total (after discounts).|
|»» total_tax|body|string|false|Line total tax (after discounts).|
|»» taxes|body|[object]|false|Line taxes.|
|»»» id|body|integer|false|Tax rate ID.|
|»»» total|body|string|false|Tax total.|
|»»» subtotal|body|string|false|Tax subtotal.|
|»» meta_data|body|[object]|false|Meta data.|
|»»» id|body|integer|false|Meta ID.|
|»»» key|body|string|false|Meta key.|
|»»» value|body|string|false|Meta value.|
|» coupon_lines|body|[object]|false|Coupons line data.|
|»» id|body|integer|false|Item ID.|
|»» code|body|string|false|Coupon code.|
|»» discount|body|string|false|Discount total.|
|»» discount_tax|body|string|false|Discount total tax.|
|»» meta_data|body|[object]|false|Meta data.|
|»»» id|body|integer|false|Meta ID.|
|»»» key|body|string|false|Meta key.|
|»»» value|body|string|false|Meta value.|
|» set_paid|body|boolean|false|Define if the order is paid. It will set the status to processing and reduce stock items.|
|» note|body|string|false|Order note content.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|pending|
|status|processing|
|status|on-hold|
|status|completed|
|status|cancelled|
|status|refunded|
|status|failed|
|status|checkout-draft|
|currency|AED|
|currency|AFN|
|currency|ALL|
|currency|AMD|
|currency|ANG|
|currency|AOA|
|currency|ARS|
|currency|AUD|
|currency|AWG|
|currency|AZN|
|currency|BAM|
|currency|BBD|
|currency|BDT|
|currency|BGN|
|currency|BHD|
|currency|BIF|
|currency|BMD|
|currency|BND|
|currency|BOB|
|currency|BRL|
|currency|BSD|
|currency|BTC|
|currency|BTN|
|currency|BWP|
|currency|BYR|
|currency|BYN|
|currency|BZD|
|currency|CAD|
|currency|CDF|
|currency|CHF|
|currency|CLP|
|currency|CNY|
|currency|COP|
|currency|CRC|
|currency|CUC|
|currency|CUP|
|currency|CVE|
|currency|CZK|
|currency|DJF|
|currency|DKK|
|currency|DOP|
|currency|DZD|
|currency|EGP|
|currency|ERN|
|currency|ETB|
|currency|EUR|
|currency|FJD|
|currency|FKP|
|currency|GBP|
|currency|GEL|
|currency|GGP|
|currency|GHS|
|currency|GIP|
|currency|GMD|
|currency|GNF|
|currency|GTQ|
|currency|GYD|
|currency|HKD|
|currency|HNL|
|currency|HRK|
|currency|HTG|
|currency|HUF|
|currency|IDR|
|currency|ILS|
|currency|IMP|
|currency|INR|
|currency|IQD|
|currency|IRR|
|currency|IRT|
|currency|ISK|
|currency|JEP|
|currency|JMD|
|currency|JOD|
|currency|JPY|
|currency|KES|
|currency|KGS|
|currency|KHR|
|currency|KMF|
|currency|KPW|
|currency|KRW|
|currency|KWD|
|currency|KYD|
|currency|KZT|
|currency|LAK|
|currency|LBP|
|currency|LKR|
|currency|LRD|
|currency|LSL|
|currency|LYD|
|currency|MAD|
|currency|MDL|
|currency|MGA|
|currency|MKD|
|currency|MMK|
|currency|MNT|
|currency|MOP|
|currency|MRU|
|currency|MUR|
|currency|MVR|
|currency|MWK|
|currency|MXN|
|currency|MYR|
|currency|MZN|
|currency|NAD|
|currency|NGN|
|currency|NIO|
|currency|NOK|
|currency|NPR|
|currency|NZD|
|currency|OMR|
|currency|PAB|
|currency|PEN|
|currency|PGK|
|currency|PHP|
|currency|PKR|
|currency|PLN|
|currency|PRB|
|currency|PYG|
|currency|QAR|
|currency|RON|
|currency|RSD|
|currency|RUB|
|currency|RWF|
|currency|SAR|
|currency|SBD|
|currency|SCR|
|currency|SDG|
|currency|SEK|
|currency|SGD|
|currency|SHP|
|currency|SLL|
|currency|SOS|
|currency|SRD|
|currency|SSP|
|currency|STN|
|currency|SYP|
|currency|SZL|
|currency|THB|
|currency|TJS|
|currency|TMT|
|currency|TND|
|currency|TOP|
|currency|TRY|
|currency|TTD|
|currency|TWD|
|currency|TZS|
|currency|UAH|
|currency|UGX|
|currency|USD|
|currency|UYU|
|currency|UZS|
|currency|VEF|
|currency|VES|
|currency|VND|
|currency|VUV|
|currency|WST|
|currency|XAF|
|currency|XCD|
|currency|XOF|
|currency|XPF|
|currency|YER|
|currency|ZAR|
|currency|ZMW|
|» status|pending|
|» status|processing|
|» status|on-hold|
|» status|completed|
|» status|cancelled|
|» status|refunded|
|» status|failed|
|» status|checkout-draft|
|» currency|AED|
|» currency|AFN|
|» currency|ALL|
|» currency|AMD|
|» currency|ANG|
|» currency|AOA|
|» currency|ARS|
|» currency|AUD|
|» currency|AWG|
|» currency|AZN|
|» currency|BAM|
|» currency|BBD|
|» currency|BDT|
|» currency|BGN|
|» currency|BHD|
|» currency|BIF|
|» currency|BMD|
|» currency|BND|
|» currency|BOB|
|» currency|BRL|
|» currency|BSD|
|» currency|BTC|
|» currency|BTN|
|» currency|BWP|
|» currency|BYR|
|» currency|BYN|
|» currency|BZD|
|» currency|CAD|
|» currency|CDF|
|» currency|CHF|
|» currency|CLP|
|» currency|CNY|
|» currency|COP|
|» currency|CRC|
|» currency|CUC|
|» currency|CUP|
|» currency|CVE|
|» currency|CZK|
|» currency|DJF|
|» currency|DKK|
|» currency|DOP|
|» currency|DZD|
|» currency|EGP|
|» currency|ERN|
|» currency|ETB|
|» currency|EUR|
|» currency|FJD|
|» currency|FKP|
|» currency|GBP|
|» currency|GEL|
|» currency|GGP|
|» currency|GHS|
|» currency|GIP|
|» currency|GMD|
|» currency|GNF|
|» currency|GTQ|
|» currency|GYD|
|» currency|HKD|
|» currency|HNL|
|» currency|HRK|
|» currency|HTG|
|» currency|HUF|
|» currency|IDR|
|» currency|ILS|
|» currency|IMP|
|» currency|INR|
|» currency|IQD|
|» currency|IRR|
|» currency|IRT|
|» currency|ISK|
|» currency|JEP|
|» currency|JMD|
|» currency|JOD|
|» currency|JPY|
|» currency|KES|
|» currency|KGS|
|» currency|KHR|
|» currency|KMF|
|» currency|KPW|
|» currency|KRW|
|» currency|KWD|
|» currency|KYD|
|» currency|KZT|
|» currency|LAK|
|» currency|LBP|
|» currency|LKR|
|» currency|LRD|
|» currency|LSL|
|» currency|LYD|
|» currency|MAD|
|» currency|MDL|
|» currency|MGA|
|» currency|MKD|
|» currency|MMK|
|» currency|MNT|
|» currency|MOP|
|» currency|MRU|
|» currency|MUR|
|» currency|MVR|
|» currency|MWK|
|» currency|MXN|
|» currency|MYR|
|» currency|MZN|
|» currency|NAD|
|» currency|NGN|
|» currency|NIO|
|» currency|NOK|
|» currency|NPR|
|» currency|NZD|
|» currency|OMR|
|» currency|PAB|
|» currency|PEN|
|» currency|PGK|
|» currency|PHP|
|» currency|PKR|
|» currency|PLN|
|» currency|PRB|
|» currency|PYG|
|» currency|QAR|
|» currency|RON|
|» currency|RSD|
|» currency|RUB|
|» currency|RWF|
|» currency|SAR|
|» currency|SBD|
|» currency|SCR|
|» currency|SDG|
|» currency|SEK|
|» currency|SGD|
|» currency|SHP|
|» currency|SLL|
|» currency|SOS|
|» currency|SRD|
|» currency|SSP|
|» currency|STN|
|» currency|SYP|
|» currency|SZL|
|» currency|THB|
|» currency|TJS|
|» currency|TMT|
|» currency|TND|
|» currency|TOP|
|» currency|TRY|
|» currency|TTD|
|» currency|TWD|
|» currency|TZS|
|» currency|UAH|
|» currency|UGX|
|» currency|USD|
|» currency|UYU|
|» currency|UZS|
|» currency|VEF|
|» currency|VES|
|» currency|VND|
|» currency|VUV|
|» currency|WST|
|» currency|XAF|
|» currency|XCD|
|» currency|XOF|
|» currency|XPF|
|» currency|YER|
|» currency|ZAR|
|» currency|ZMW|
|»» tax_status|taxable|
|»» tax_status|none|

<h3 id="post__orders_{id}_notes-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__orders_{id}_notes_{note_id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/orders/{id}/notes/{note_id}', array(
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

r = requests.get('http://dokan-sample.test/orders/{id}/notes/{note_id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/orders/{id}/notes/{note_id}',
  params: {
  }

p JSON.parse(result)

```

`GET /orders/{id}/notes/{note_id}`

<h3 id="get__orders_{id}_notes_{note_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|note_id|path|integer|true|Unique identifier for the note object.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Order id to search order|
|seller_id|query|integer|false|Orders belongs to specific seller|
|status|query|string|false|Order status.|
|date_created|query|string(date-time)|false|The date the order was created, in the site's timezone.|
|customer_id|query|string|false|User ID who owns the order. 0 for guests.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__orders_{id}_notes_{note_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__orders_{id}_notes_{note_id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/orders/{id}/notes/{note_id}', array(
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

r = requests.delete('http://dokan-sample.test/orders/{id}/notes/{note_id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/orders/{id}/notes/{note_id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /orders/{id}/notes/{note_id}`

<h3 id="delete__orders_{id}_notes_{note_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|note_id|path|integer|true|Unique identifier for the note object.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Order id to search order|
|seller_id|query|integer|false|Orders belongs to specific seller|
|status|query|string|false|Order status.|
|date_created|query|string(date-time)|false|The date the order was created, in the site's timezone.|
|customer_id|query|string|false|User ID who owns the order. 0 for guests.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="delete__orders_{id}_notes_{note_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__orders_summary

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/orders/summary', array(
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

r = requests.get('http://dokan-sample.test/orders/summary')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/orders/summary',
  params: {
  }

p JSON.parse(result)

```

`GET /orders/summary`

<h3 id="get__orders_summary-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Order id to search order|
|seller_id|query|integer|false|Orders belongs to specific seller|
|status|query|string|false|Order status.|
|date_created|query|string(date-time)|false|The date the order was created, in the site's timezone.|
|customer_id|query|string|false|User ID who owns the order. 0 for guests.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__orders_summary-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

