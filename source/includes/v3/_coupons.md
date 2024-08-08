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

## get__coupons

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/coupons', array(
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

r = requests.get('http://dokan-sample.test/coupons')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/coupons',
  params: {
  }

p JSON.parse(result)

```

`GET /coupons`

<h3 id="get__coupons-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|code|query|string|false|Limit result set to resources with a specific code.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__coupons-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__coupons

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
    $response = $client->request('POST','http://dokan-sample.test/coupons', array(
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

r = requests.post('http://dokan-sample.test/coupons', params={
  'code': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/coupons',
  params: {
  'code' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /coupons`

> Body parameter

```json
{
  "code": "string",
  "amount": "string",
  "discount_type": "percent",
  "description": "string",
  "date_expires": "string",
  "date_expires_gmt": "string",
  "individual_use": true,
  "product_ids": [
    0
  ],
  "excluded_product_ids": [
    0
  ],
  "usage_limit": 0,
  "usage_limit_per_user": 0,
  "limit_usage_to_x_items": 0,
  "free_shipping": true,
  "product_categories": [
    0
  ],
  "excluded_product_categories": [
    0
  ],
  "exclude_sale_items": true,
  "minimum_amount": "string",
  "maximum_amount": "string",
  "email_restrictions": [
    "string"
  ],
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="post__coupons-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|code|query|string|true|Coupon code.|
|amount|query|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|discount_type|query|string|false|Determines the type of discount that will be applied.|
|description|query|string|false|Coupon description.|
|date_expires|query|string|false|The date the coupon expires, in the site's timezone.|
|date_expires_gmt|query|string|false|The date the coupon expires, as GMT.|
|individual_use|query|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|product_ids|query|array[integer]|false|List of product IDs the coupon can be used on.|
|excluded_product_ids|query|array[integer]|false|List of product IDs the coupon cannot be used on.|
|usage_limit|query|integer|false|How many times the coupon can be used in total.|
|usage_limit_per_user|query|integer|false|How many times the coupon can be used per customer.|
|limit_usage_to_x_items|query|integer|false|Max number of items in the cart the coupon can be applied to.|
|free_shipping|query|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|product_categories|query|array[integer]|false|List of category IDs the coupon applies to.|
|excluded_product_categories|query|array[integer]|false|List of category IDs the coupon does not apply to.|
|exclude_sale_items|query|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|minimum_amount|query|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|maximum_amount|query|string|false|Maximum order amount allowed when using the coupon.|
|email_restrictions|query|array[string]|false|List of email addresses that can use this coupon.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» code|body|string|false|Coupon code.|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» discount_type|body|string|false|Determines the type of discount that will be applied.|
|» description|body|string|false|Coupon description.|
|» date_expires|body|string|false|The date the coupon expires, in the site's timezone.|
|» date_expires_gmt|body|string|false|The date the coupon expires, as GMT.|
|» individual_use|body|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|» product_ids|body|[integer]|false|List of product IDs the coupon can be used on.|
|» excluded_product_ids|body|[integer]|false|List of product IDs the coupon cannot be used on.|
|» usage_limit|body|integer|false|How many times the coupon can be used in total.|
|» usage_limit_per_user|body|integer|false|How many times the coupon can be used per customer.|
|» limit_usage_to_x_items|body|integer|false|Max number of items in the cart the coupon can be applied to.|
|» free_shipping|body|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|» product_categories|body|[integer]|false|List of category IDs the coupon applies to.|
|» excluded_product_categories|body|[integer]|false|List of category IDs the coupon does not apply to.|
|» exclude_sale_items|body|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|» minimum_amount|body|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|» maximum_amount|body|string|false|Maximum order amount allowed when using the coupon.|
|» email_restrictions|body|[string]|false|List of email addresses that can use this coupon.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|discount_type|percent|
|discount_type|fixed_cart|
|discount_type|fixed_product|
|» discount_type|percent|
|» discount_type|fixed_cart|
|» discount_type|fixed_product|

<h3 id="post__coupons-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__coupons_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/coupons/{id}', array(
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

r = requests.get('http://dokan-sample.test/coupons/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/coupons/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /coupons/{id}`

<h3 id="get__coupons_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__coupons_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__coupons_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/coupons/{id}', array(
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

r = requests.post('http://dokan-sample.test/coupons/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/coupons/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /coupons/{id}`

> Body parameter

```json
{
  "code": "string",
  "amount": "string",
  "discount_type": "percent",
  "description": "string",
  "date_expires": "string",
  "date_expires_gmt": "string",
  "individual_use": true,
  "product_ids": [
    0
  ],
  "excluded_product_ids": [
    0
  ],
  "usage_limit": 0,
  "usage_limit_per_user": 0,
  "limit_usage_to_x_items": 0,
  "free_shipping": true,
  "product_categories": [
    0
  ],
  "excluded_product_categories": [
    0
  ],
  "exclude_sale_items": true,
  "minimum_amount": "string",
  "maximum_amount": "string",
  "email_restrictions": [
    "string"
  ],
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="post__coupons_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|code|query|string|false|Coupon code.|
|amount|query|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|discount_type|query|string|false|Determines the type of discount that will be applied.|
|description|query|string|false|Coupon description.|
|date_expires|query|string|false|The date the coupon expires, in the site's timezone.|
|date_expires_gmt|query|string|false|The date the coupon expires, as GMT.|
|individual_use|query|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|product_ids|query|array[integer]|false|List of product IDs the coupon can be used on.|
|excluded_product_ids|query|array[integer]|false|List of product IDs the coupon cannot be used on.|
|usage_limit|query|integer|false|How many times the coupon can be used in total.|
|usage_limit_per_user|query|integer|false|How many times the coupon can be used per customer.|
|limit_usage_to_x_items|query|integer|false|Max number of items in the cart the coupon can be applied to.|
|free_shipping|query|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|product_categories|query|array[integer]|false|List of category IDs the coupon applies to.|
|excluded_product_categories|query|array[integer]|false|List of category IDs the coupon does not apply to.|
|exclude_sale_items|query|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|minimum_amount|query|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|maximum_amount|query|string|false|Maximum order amount allowed when using the coupon.|
|email_restrictions|query|array[string]|false|List of email addresses that can use this coupon.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» code|body|string|false|Coupon code.|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» discount_type|body|string|false|Determines the type of discount that will be applied.|
|» description|body|string|false|Coupon description.|
|» date_expires|body|string|false|The date the coupon expires, in the site's timezone.|
|» date_expires_gmt|body|string|false|The date the coupon expires, as GMT.|
|» individual_use|body|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|» product_ids|body|[integer]|false|List of product IDs the coupon can be used on.|
|» excluded_product_ids|body|[integer]|false|List of product IDs the coupon cannot be used on.|
|» usage_limit|body|integer|false|How many times the coupon can be used in total.|
|» usage_limit_per_user|body|integer|false|How many times the coupon can be used per customer.|
|» limit_usage_to_x_items|body|integer|false|Max number of items in the cart the coupon can be applied to.|
|» free_shipping|body|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|» product_categories|body|[integer]|false|List of category IDs the coupon applies to.|
|» excluded_product_categories|body|[integer]|false|List of category IDs the coupon does not apply to.|
|» exclude_sale_items|body|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|» minimum_amount|body|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|» maximum_amount|body|string|false|Maximum order amount allowed when using the coupon.|
|» email_restrictions|body|[string]|false|List of email addresses that can use this coupon.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|discount_type|percent|
|discount_type|fixed_cart|
|discount_type|fixed_product|
|» discount_type|percent|
|» discount_type|fixed_cart|
|» discount_type|fixed_product|

<h3 id="post__coupons_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__coupons_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/coupons/{id}', array(
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

r = requests.put('http://dokan-sample.test/coupons/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/coupons/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /coupons/{id}`

> Body parameter

```json
{
  "code": "string",
  "amount": "string",
  "discount_type": "percent",
  "description": "string",
  "date_expires": "string",
  "date_expires_gmt": "string",
  "individual_use": true,
  "product_ids": [
    0
  ],
  "excluded_product_ids": [
    0
  ],
  "usage_limit": 0,
  "usage_limit_per_user": 0,
  "limit_usage_to_x_items": 0,
  "free_shipping": true,
  "product_categories": [
    0
  ],
  "excluded_product_categories": [
    0
  ],
  "exclude_sale_items": true,
  "minimum_amount": "string",
  "maximum_amount": "string",
  "email_restrictions": [
    "string"
  ],
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="put__coupons_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|code|query|string|false|Coupon code.|
|amount|query|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|discount_type|query|string|false|Determines the type of discount that will be applied.|
|description|query|string|false|Coupon description.|
|date_expires|query|string|false|The date the coupon expires, in the site's timezone.|
|date_expires_gmt|query|string|false|The date the coupon expires, as GMT.|
|individual_use|query|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|product_ids|query|array[integer]|false|List of product IDs the coupon can be used on.|
|excluded_product_ids|query|array[integer]|false|List of product IDs the coupon cannot be used on.|
|usage_limit|query|integer|false|How many times the coupon can be used in total.|
|usage_limit_per_user|query|integer|false|How many times the coupon can be used per customer.|
|limit_usage_to_x_items|query|integer|false|Max number of items in the cart the coupon can be applied to.|
|free_shipping|query|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|product_categories|query|array[integer]|false|List of category IDs the coupon applies to.|
|excluded_product_categories|query|array[integer]|false|List of category IDs the coupon does not apply to.|
|exclude_sale_items|query|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|minimum_amount|query|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|maximum_amount|query|string|false|Maximum order amount allowed when using the coupon.|
|email_restrictions|query|array[string]|false|List of email addresses that can use this coupon.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» code|body|string|false|Coupon code.|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» discount_type|body|string|false|Determines the type of discount that will be applied.|
|» description|body|string|false|Coupon description.|
|» date_expires|body|string|false|The date the coupon expires, in the site's timezone.|
|» date_expires_gmt|body|string|false|The date the coupon expires, as GMT.|
|» individual_use|body|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|» product_ids|body|[integer]|false|List of product IDs the coupon can be used on.|
|» excluded_product_ids|body|[integer]|false|List of product IDs the coupon cannot be used on.|
|» usage_limit|body|integer|false|How many times the coupon can be used in total.|
|» usage_limit_per_user|body|integer|false|How many times the coupon can be used per customer.|
|» limit_usage_to_x_items|body|integer|false|Max number of items in the cart the coupon can be applied to.|
|» free_shipping|body|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|» product_categories|body|[integer]|false|List of category IDs the coupon applies to.|
|» excluded_product_categories|body|[integer]|false|List of category IDs the coupon does not apply to.|
|» exclude_sale_items|body|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|» minimum_amount|body|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|» maximum_amount|body|string|false|Maximum order amount allowed when using the coupon.|
|» email_restrictions|body|[string]|false|List of email addresses that can use this coupon.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|discount_type|percent|
|discount_type|fixed_cart|
|discount_type|fixed_product|
|» discount_type|percent|
|» discount_type|fixed_cart|
|» discount_type|fixed_product|

<h3 id="put__coupons_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__coupons_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/coupons/{id}', array(
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

r = requests.patch('http://dokan-sample.test/coupons/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/coupons/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /coupons/{id}`

> Body parameter

```json
{
  "code": "string",
  "amount": "string",
  "discount_type": "percent",
  "description": "string",
  "date_expires": "string",
  "date_expires_gmt": "string",
  "individual_use": true,
  "product_ids": [
    0
  ],
  "excluded_product_ids": [
    0
  ],
  "usage_limit": 0,
  "usage_limit_per_user": 0,
  "limit_usage_to_x_items": 0,
  "free_shipping": true,
  "product_categories": [
    0
  ],
  "excluded_product_categories": [
    0
  ],
  "exclude_sale_items": true,
  "minimum_amount": "string",
  "maximum_amount": "string",
  "email_restrictions": [
    "string"
  ],
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="patch__coupons_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|code|query|string|false|Coupon code.|
|amount|query|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|discount_type|query|string|false|Determines the type of discount that will be applied.|
|description|query|string|false|Coupon description.|
|date_expires|query|string|false|The date the coupon expires, in the site's timezone.|
|date_expires_gmt|query|string|false|The date the coupon expires, as GMT.|
|individual_use|query|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|product_ids|query|array[integer]|false|List of product IDs the coupon can be used on.|
|excluded_product_ids|query|array[integer]|false|List of product IDs the coupon cannot be used on.|
|usage_limit|query|integer|false|How many times the coupon can be used in total.|
|usage_limit_per_user|query|integer|false|How many times the coupon can be used per customer.|
|limit_usage_to_x_items|query|integer|false|Max number of items in the cart the coupon can be applied to.|
|free_shipping|query|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|product_categories|query|array[integer]|false|List of category IDs the coupon applies to.|
|excluded_product_categories|query|array[integer]|false|List of category IDs the coupon does not apply to.|
|exclude_sale_items|query|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|minimum_amount|query|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|maximum_amount|query|string|false|Maximum order amount allowed when using the coupon.|
|email_restrictions|query|array[string]|false|List of email addresses that can use this coupon.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» code|body|string|false|Coupon code.|
|» amount|body|string|false|The amount of discount. Should always be numeric, even if setting a percentage.|
|» discount_type|body|string|false|Determines the type of discount that will be applied.|
|» description|body|string|false|Coupon description.|
|» date_expires|body|string|false|The date the coupon expires, in the site's timezone.|
|» date_expires_gmt|body|string|false|The date the coupon expires, as GMT.|
|» individual_use|body|boolean|false|If true, the coupon can only be used individually. Other applied coupons will be removed from the cart.|
|» product_ids|body|[integer]|false|List of product IDs the coupon can be used on.|
|» excluded_product_ids|body|[integer]|false|List of product IDs the coupon cannot be used on.|
|» usage_limit|body|integer|false|How many times the coupon can be used in total.|
|» usage_limit_per_user|body|integer|false|How many times the coupon can be used per customer.|
|» limit_usage_to_x_items|body|integer|false|Max number of items in the cart the coupon can be applied to.|
|» free_shipping|body|boolean|false|If true and if the free shipping method requires a coupon, this coupon will enable free shipping.|
|» product_categories|body|[integer]|false|List of category IDs the coupon applies to.|
|» excluded_product_categories|body|[integer]|false|List of category IDs the coupon does not apply to.|
|» exclude_sale_items|body|boolean|false|If true, this coupon will not be applied to items that have sale prices.|
|» minimum_amount|body|string|false|Minimum order amount that needs to be in the cart before coupon applies.|
|» maximum_amount|body|string|false|Maximum order amount allowed when using the coupon.|
|» email_restrictions|body|[string]|false|List of email addresses that can use this coupon.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|discount_type|percent|
|discount_type|fixed_cart|
|discount_type|fixed_product|
|» discount_type|percent|
|» discount_type|fixed_cart|
|» discount_type|fixed_product|

<h3 id="patch__coupons_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__coupons_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/coupons/{id}', array(
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

r = requests.delete('http://dokan-sample.test/coupons/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/coupons/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /coupons/{id}`

<h3 id="delete__coupons_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|

<h3 id="delete__coupons_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

