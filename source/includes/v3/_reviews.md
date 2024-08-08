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

## get__reviews

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/reviews', array(
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

r = requests.get('http://dokan-sample.test/reviews')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/reviews',
  params: {
  }

p JSON.parse(result)

```

`GET /reviews`

<h3 id="get__reviews-parameters">Parameters</h3>

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

<h3 id="get__reviews-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__reviews_summary

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/reviews/summary', array(
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

r = requests.get('http://dokan-sample.test/reviews/summary')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/reviews/summary',
  params: {
  }

p JSON.parse(result)

```

`GET /reviews/summary`

<h3 id="get__reviews_summary-parameters">Parameters</h3>

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

<h3 id="get__reviews_summary-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__reviews_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/reviews/{id}', array(
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

r = requests.post('http://dokan-sample.test/reviews/{id}', params={
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

result = RestClient.post 'http://dokan-sample.test/reviews/{id}',
  params: {
  'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /reviews/{id}`

> Body parameter

```json
{
  "status": "string"
}
```

<h3 id="post__reviews_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|status|query|string|true|Review Status|
|body|body|object|true|none|
|» status|body|string|false|Review Status|

<h3 id="post__reviews_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__reviews_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/reviews/{id}', array(
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

r = requests.put('http://dokan-sample.test/reviews/{id}', params={
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

result = RestClient.put 'http://dokan-sample.test/reviews/{id}',
  params: {
  'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`PUT /reviews/{id}`

> Body parameter

```json
{
  "status": "string"
}
```

<h3 id="put__reviews_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|status|query|string|true|Review Status|
|body|body|object|true|none|
|» status|body|string|false|Review Status|

<h3 id="put__reviews_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__reviews_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/reviews/{id}', array(
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

r = requests.patch('http://dokan-sample.test/reviews/{id}', params={
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

result = RestClient.patch 'http://dokan-sample.test/reviews/{id}',
  params: {
  'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`PATCH /reviews/{id}`

> Body parameter

```json
{
  "status": "string"
}
```

<h3 id="patch__reviews_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|status|query|string|true|Review Status|
|body|body|object|true|none|
|» status|body|string|false|Review Status|

<h3 id="patch__reviews_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_{product_id}_variations

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/{product_id}/variations', array(
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

r = requests.get('http://dokan-sample.test/products/{product_id}/variations')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/{product_id}/variations',
  params: {
  }

p JSON.parse(result)

```

`GET /products/{product_id}/variations`

<h3 id="get__products_{product_id}_variations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Unique identifier for the variable product.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__products_{product_id}_variations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_{product_id}_variations

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
    $response = $client->request('POST','http://dokan-sample.test/products/{product_id}/variations', array(
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

r = requests.post('http://dokan-sample.test/products/{product_id}/variations', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/{product_id}/variations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/{product_id}/variations`

> Body parameter

```json
{
  "description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
  "visible": true,
  "virtual": true,
  "downloadable": true,
  "downloads": [
    {
      "id": "string",
      "name": "string",
      "file": "string"
    }
  ],
  "download_limit": 0,
  "download_expiry": 0,
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": "string",
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "image": {
    "id": 0,
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "src": "http://example.com",
    "name": "string",
    "alt": "string",
    "position": 0
  },
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "menu_order": 0,
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="post__products_{product_id}_variations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Unique identifier for the variable product.|
|description|query|string|false|Variation description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Variation regular price.|
|sale_price|query|string|false|Variation sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|visible|query|boolean|false|Define if the variation is visible on the product's page.|
|virtual|query|boolean|false|If the variation is virtual.|
|downloadable|query|boolean|false|If the variation is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|string|false|Stock management at variation level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|weight|query|string|false|Variation weight (kg).|
|dimensions|query|object|false|Variation dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|image|query|object|false|Variation image data.|
|attributes|query|array[object]|false|List of attributes.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» description|body|string|false|Variation description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Variation regular price.|
|» sale_price|body|string|false|Variation sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» visible|body|boolean|false|Define if the variation is visible on the product's page.|
|» virtual|body|boolean|false|If the variation is virtual.|
|» downloadable|body|boolean|false|If the variation is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|string|false|Stock management at variation level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» weight|body|string|false|Variation weight (kg).|
|» dimensions|body|object|false|Variation dimensions.|
|»» length|body|string|false|Variation length (cm).|
|»» width|body|string|false|Variation width (cm).|
|»» height|body|string|false|Variation height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» image|body|object|false|Variation image data.|
|»» id|body|integer|false|Image ID.|
|»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»» src|body|string(uri)|false|Image URL.|
|»» name|body|string|false|Image name.|
|»» alt|body|string|false|Image alternative text.|
|»» position|body|integer|false|Image position. 0 means that the image is featured.|
|» attributes|body|[object]|false|List of attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="post__products_{product_id}_variations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_{product_id}_variations_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/{product_id}/variations/{id}', array(
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

r = requests.get('http://dokan-sample.test/products/{product_id}/variations/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/{product_id}/variations/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /products/{product_id}/variations/{id}`

<h3 id="get__products_{product_id}_variations_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Unique identifier for the variable product.|
|id|path|integer|true|Unique identifier for the variation.|

<h3 id="get__products_{product_id}_variations_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_{product_id}_variations_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/products/{product_id}/variations/{id}', array(
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

r = requests.post('http://dokan-sample.test/products/{product_id}/variations/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/{product_id}/variations/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/{product_id}/variations/{id}`

> Body parameter

```json
{
  "description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
  "visible": true,
  "virtual": true,
  "downloadable": true,
  "downloads": [
    {
      "id": "string",
      "name": "string",
      "file": "string"
    }
  ],
  "download_limit": 0,
  "download_expiry": 0,
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": "string",
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "image": {
    "id": 0,
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "src": "http://example.com",
    "name": "string",
    "alt": "string",
    "position": 0
  },
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "menu_order": 0,
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="post__products_{product_id}_variations_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Unique identifier for the variable product.|
|id|path|integer|true|Unique identifier for the variation.|
|description|query|string|false|Variation description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Variation regular price.|
|sale_price|query|string|false|Variation sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|visible|query|boolean|false|Define if the variation is visible on the product's page.|
|virtual|query|boolean|false|If the variation is virtual.|
|downloadable|query|boolean|false|If the variation is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|string|false|Stock management at variation level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|weight|query|string|false|Variation weight (kg).|
|dimensions|query|object|false|Variation dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|image|query|object|false|Variation image data.|
|attributes|query|array[object]|false|List of attributes.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» description|body|string|false|Variation description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Variation regular price.|
|» sale_price|body|string|false|Variation sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» visible|body|boolean|false|Define if the variation is visible on the product's page.|
|» virtual|body|boolean|false|If the variation is virtual.|
|» downloadable|body|boolean|false|If the variation is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|string|false|Stock management at variation level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» weight|body|string|false|Variation weight (kg).|
|» dimensions|body|object|false|Variation dimensions.|
|»» length|body|string|false|Variation length (cm).|
|»» width|body|string|false|Variation width (cm).|
|»» height|body|string|false|Variation height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» image|body|object|false|Variation image data.|
|»» id|body|integer|false|Image ID.|
|»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»» src|body|string(uri)|false|Image URL.|
|»» name|body|string|false|Image name.|
|»» alt|body|string|false|Image alternative text.|
|»» position|body|integer|false|Image position. 0 means that the image is featured.|
|» attributes|body|[object]|false|List of attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="post__products_{product_id}_variations_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_{product_id}_variations_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/products/{product_id}/variations/{id}', array(
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

r = requests.put('http://dokan-sample.test/products/{product_id}/variations/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/products/{product_id}/variations/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /products/{product_id}/variations/{id}`

> Body parameter

```json
{
  "description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
  "visible": true,
  "virtual": true,
  "downloadable": true,
  "downloads": [
    {
      "id": "string",
      "name": "string",
      "file": "string"
    }
  ],
  "download_limit": 0,
  "download_expiry": 0,
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": "string",
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "image": {
    "id": 0,
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "src": "http://example.com",
    "name": "string",
    "alt": "string",
    "position": 0
  },
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "menu_order": 0,
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="put__products_{product_id}_variations_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Unique identifier for the variable product.|
|id|path|integer|true|Unique identifier for the variation.|
|description|query|string|false|Variation description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Variation regular price.|
|sale_price|query|string|false|Variation sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|visible|query|boolean|false|Define if the variation is visible on the product's page.|
|virtual|query|boolean|false|If the variation is virtual.|
|downloadable|query|boolean|false|If the variation is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|string|false|Stock management at variation level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|weight|query|string|false|Variation weight (kg).|
|dimensions|query|object|false|Variation dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|image|query|object|false|Variation image data.|
|attributes|query|array[object]|false|List of attributes.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» description|body|string|false|Variation description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Variation regular price.|
|» sale_price|body|string|false|Variation sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» visible|body|boolean|false|Define if the variation is visible on the product's page.|
|» virtual|body|boolean|false|If the variation is virtual.|
|» downloadable|body|boolean|false|If the variation is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|string|false|Stock management at variation level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» weight|body|string|false|Variation weight (kg).|
|» dimensions|body|object|false|Variation dimensions.|
|»» length|body|string|false|Variation length (cm).|
|»» width|body|string|false|Variation width (cm).|
|»» height|body|string|false|Variation height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» image|body|object|false|Variation image data.|
|»» id|body|integer|false|Image ID.|
|»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»» src|body|string(uri)|false|Image URL.|
|»» name|body|string|false|Image name.|
|»» alt|body|string|false|Image alternative text.|
|»» position|body|integer|false|Image position. 0 means that the image is featured.|
|» attributes|body|[object]|false|List of attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="put__products_{product_id}_variations_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_{product_id}_variations_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/{product_id}/variations/{id}', array(
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

r = requests.patch('http://dokan-sample.test/products/{product_id}/variations/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/products/{product_id}/variations/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /products/{product_id}/variations/{id}`

> Body parameter

```json
{
  "description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
  "visible": true,
  "virtual": true,
  "downloadable": true,
  "downloads": [
    {
      "id": "string",
      "name": "string",
      "file": "string"
    }
  ],
  "download_limit": 0,
  "download_expiry": 0,
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": "string",
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "image": {
    "id": 0,
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "src": "http://example.com",
    "name": "string",
    "alt": "string",
    "position": 0
  },
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "menu_order": 0,
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="patch__products_{product_id}_variations_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Unique identifier for the variable product.|
|id|path|integer|true|Unique identifier for the variation.|
|description|query|string|false|Variation description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Variation regular price.|
|sale_price|query|string|false|Variation sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|visible|query|boolean|false|Define if the variation is visible on the product's page.|
|virtual|query|boolean|false|If the variation is virtual.|
|downloadable|query|boolean|false|If the variation is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|string|false|Stock management at variation level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|weight|query|string|false|Variation weight (kg).|
|dimensions|query|object|false|Variation dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|image|query|object|false|Variation image data.|
|attributes|query|array[object]|false|List of attributes.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» description|body|string|false|Variation description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Variation regular price.|
|» sale_price|body|string|false|Variation sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» visible|body|boolean|false|Define if the variation is visible on the product's page.|
|» virtual|body|boolean|false|If the variation is virtual.|
|» downloadable|body|boolean|false|If the variation is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|string|false|Stock management at variation level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» weight|body|string|false|Variation weight (kg).|
|» dimensions|body|object|false|Variation dimensions.|
|»» length|body|string|false|Variation length (cm).|
|»» width|body|string|false|Variation width (cm).|
|»» height|body|string|false|Variation height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» image|body|object|false|Variation image data.|
|»» id|body|integer|false|Image ID.|
|»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»» src|body|string(uri)|false|Image URL.|
|»» name|body|string|false|Image name.|
|»» alt|body|string|false|Image alternative text.|
|»» position|body|integer|false|Image position. 0 means that the image is featured.|
|» attributes|body|[object]|false|List of attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="patch__products_{product_id}_variations_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__products_{product_id}_variations_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/products/{product_id}/variations/{id}', array(
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

r = requests.delete('http://dokan-sample.test/products/{product_id}/variations/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/products/{product_id}/variations/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /products/{product_id}/variations/{id}`

<h3 id="delete__products_{product_id}_variations_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Unique identifier for the variable product.|
|id|path|integer|true|Unique identifier for the variation.|

<h3 id="delete__products_{product_id}_variations_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_{product_id}_variations_batch

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
    $response = $client->request('POST','http://dokan-sample.test/products/{product_id}/variations/batch', array(
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

r = requests.post('http://dokan-sample.test/products/{product_id}/variations/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/{product_id}/variations/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/{product_id}/variations/batch`

> Body parameter

```json
{
  "description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
  "visible": true,
  "virtual": true,
  "downloadable": true,
  "downloads": [
    {
      "id": "string",
      "name": "string",
      "file": "string"
    }
  ],
  "download_limit": 0,
  "download_expiry": 0,
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": "string",
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "image": {
    "id": 0,
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "src": "http://example.com",
    "name": "string",
    "alt": "string",
    "position": 0
  },
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "menu_order": 0,
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="post__products_{product_id}_variations_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Product ID for which variations will be managed.|
|description|query|string|false|Variation description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Variation regular price.|
|sale_price|query|string|false|Variation sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|visible|query|boolean|false|Define if the variation is visible on the product's page.|
|virtual|query|boolean|false|If the variation is virtual.|
|downloadable|query|boolean|false|If the variation is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|string|false|Stock management at variation level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|weight|query|string|false|Variation weight (kg).|
|dimensions|query|object|false|Variation dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|image|query|object|false|Variation image data.|
|attributes|query|array[object]|false|List of attributes.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» description|body|string|false|Variation description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Variation regular price.|
|» sale_price|body|string|false|Variation sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» visible|body|boolean|false|Define if the variation is visible on the product's page.|
|» virtual|body|boolean|false|If the variation is virtual.|
|» downloadable|body|boolean|false|If the variation is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|string|false|Stock management at variation level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» weight|body|string|false|Variation weight (kg).|
|» dimensions|body|object|false|Variation dimensions.|
|»» length|body|string|false|Variation length (cm).|
|»» width|body|string|false|Variation width (cm).|
|»» height|body|string|false|Variation height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» image|body|object|false|Variation image data.|
|»» id|body|integer|false|Image ID.|
|»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»» src|body|string(uri)|false|Image URL.|
|»» name|body|string|false|Image name.|
|»» alt|body|string|false|Image alternative text.|
|»» position|body|integer|false|Image position. 0 means that the image is featured.|
|» attributes|body|[object]|false|List of attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="post__products_{product_id}_variations_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_{product_id}_variations_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/products/{product_id}/variations/batch', array(
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

r = requests.put('http://dokan-sample.test/products/{product_id}/variations/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/products/{product_id}/variations/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /products/{product_id}/variations/batch`

> Body parameter

```json
{
  "description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
  "visible": true,
  "virtual": true,
  "downloadable": true,
  "downloads": [
    {
      "id": "string",
      "name": "string",
      "file": "string"
    }
  ],
  "download_limit": 0,
  "download_expiry": 0,
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": "string",
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "image": {
    "id": 0,
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "src": "http://example.com",
    "name": "string",
    "alt": "string",
    "position": 0
  },
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "menu_order": 0,
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="put__products_{product_id}_variations_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Product ID for which variations will be managed.|
|description|query|string|false|Variation description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Variation regular price.|
|sale_price|query|string|false|Variation sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|visible|query|boolean|false|Define if the variation is visible on the product's page.|
|virtual|query|boolean|false|If the variation is virtual.|
|downloadable|query|boolean|false|If the variation is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|string|false|Stock management at variation level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|weight|query|string|false|Variation weight (kg).|
|dimensions|query|object|false|Variation dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|image|query|object|false|Variation image data.|
|attributes|query|array[object]|false|List of attributes.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» description|body|string|false|Variation description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Variation regular price.|
|» sale_price|body|string|false|Variation sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» visible|body|boolean|false|Define if the variation is visible on the product's page.|
|» virtual|body|boolean|false|If the variation is virtual.|
|» downloadable|body|boolean|false|If the variation is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|string|false|Stock management at variation level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» weight|body|string|false|Variation weight (kg).|
|» dimensions|body|object|false|Variation dimensions.|
|»» length|body|string|false|Variation length (cm).|
|»» width|body|string|false|Variation width (cm).|
|»» height|body|string|false|Variation height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» image|body|object|false|Variation image data.|
|»» id|body|integer|false|Image ID.|
|»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»» src|body|string(uri)|false|Image URL.|
|»» name|body|string|false|Image name.|
|»» alt|body|string|false|Image alternative text.|
|»» position|body|integer|false|Image position. 0 means that the image is featured.|
|» attributes|body|[object]|false|List of attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="put__products_{product_id}_variations_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_{product_id}_variations_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/{product_id}/variations/batch', array(
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

r = requests.patch('http://dokan-sample.test/products/{product_id}/variations/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/products/{product_id}/variations/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /products/{product_id}/variations/batch`

> Body parameter

```json
{
  "description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
  "visible": true,
  "virtual": true,
  "downloadable": true,
  "downloads": [
    {
      "id": "string",
      "name": "string",
      "file": "string"
    }
  ],
  "download_limit": 0,
  "download_expiry": 0,
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": "string",
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "image": {
    "id": 0,
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "src": "http://example.com",
    "name": "string",
    "alt": "string",
    "position": 0
  },
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "menu_order": 0,
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": "string"
    }
  ]
}
```

<h3 id="patch__products_{product_id}_variations_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|product_id|path|integer|true|Product ID for which variations will be managed.|
|description|query|string|false|Variation description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Variation regular price.|
|sale_price|query|string|false|Variation sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|visible|query|boolean|false|Define if the variation is visible on the product's page.|
|virtual|query|boolean|false|If the variation is virtual.|
|downloadable|query|boolean|false|If the variation is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|string|false|Stock management at variation level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|weight|query|string|false|Variation weight (kg).|
|dimensions|query|object|false|Variation dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|image|query|object|false|Variation image data.|
|attributes|query|array[object]|false|List of attributes.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» description|body|string|false|Variation description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Variation regular price.|
|» sale_price|body|string|false|Variation sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» visible|body|boolean|false|Define if the variation is visible on the product's page.|
|» virtual|body|boolean|false|If the variation is virtual.|
|» downloadable|body|boolean|false|If the variation is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|string|false|Stock management at variation level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» weight|body|string|false|Variation weight (kg).|
|» dimensions|body|object|false|Variation dimensions.|
|»» length|body|string|false|Variation length (cm).|
|»» width|body|string|false|Variation width (cm).|
|»» height|body|string|false|Variation height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» image|body|object|false|Variation image data.|
|»» id|body|integer|false|Image ID.|
|»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»» src|body|string(uri)|false|Image URL.|
|»» name|body|string|false|Image name.|
|»» alt|body|string|false|Image alternative text.|
|»» position|body|integer|false|Image position. 0 means that the image is featured.|
|» attributes|body|[object]|false|List of attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="patch__products_{product_id}_variations_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__stores_{id}_stats

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/stores/{id}/stats', array(
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

r = requests.get('http://dokan-sample.test/stores/{id}/stats')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/stores/{id}/stats',
  params: {
  }

p JSON.parse(result)

```

`GET /stores/{id}/stats`

<h3 id="get__stores_{id}_stats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|

<h3 id="get__stores_{id}_stats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__stores_{id}_email

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
    $response = $client->request('POST','http://dokan-sample.test/stores/{id}/email', array(
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

r = requests.post('http://dokan-sample.test/stores/{id}/email', params={
  'subject': 'string',  'body': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/stores/{id}/email',
  params: {
  'subject' => 'string',
'body' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /stores/{id}/email`

> Body parameter

```json
{
  "subject": "string",
  "body": "string",
  "context": "string",
  "page": 0,
  "per_page": 0,
  "search": "string"
}
```

<h3 id="post__stores_{id}_email-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|subject|query|string|true|Subject of the email.|
|body|query|string|true|Body of the email.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|body|body|object|true|none|
|» subject|body|string|false|Subject of the email.|
|» body|body|string|false|Body of the email.|
|» context|body|string|false|Scope under which the request is made; determines fields present in response.|
|» page|body|integer|false|Current page of the collection.|
|» per_page|body|integer|false|Maximum number of items to be returned in result set.|
|» search|body|string|false|Limit results to those matching a string.|

<h3 id="post__stores_{id}_email-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__stores_current-visitor

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/stores/current-visitor', array(
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

r = requests.get('http://dokan-sample.test/stores/current-visitor')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/stores/current-visitor',
  params: {
  }

p JSON.parse(result)

```

`GET /stores/current-visitor`

<h3 id="get__stores_current-visitor-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|

<h3 id="get__stores_current-visitor-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__admin_modules

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/admin/modules', array(
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

r = requests.get('http://dokan-sample.test/admin/modules')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/admin/modules',
  params: {
  }

p JSON.parse(result)

```

`GET /admin/modules`

<h3 id="get__admin_modules-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__admin_modules_activate

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
    $response = $client->request('POST','http://dokan-sample.test/admin/modules/activate', array(
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

r = requests.post('http://dokan-sample.test/admin/modules/activate', params={
  'module': [
  "string"
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

result = RestClient.post 'http://dokan-sample.test/admin/modules/activate',
  params: {
  'module' => 'array[string]'
}, headers: headers

p JSON.parse(result)

```

`POST /admin/modules/activate`

> Body parameter

```json
{
  "module": [
    "string"
  ]
}
```

<h3 id="post__admin_modules_activate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|module|query|array[string]|true|Basename of the module as array|
|body|body|object|true|none|
|» module|body|[string]|false|Basename of the module as array|

<h3 id="post__admin_modules_activate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__admin_modules_activate

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
    $response = $client->request('PUT','http://dokan-sample.test/admin/modules/activate', array(
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

r = requests.put('http://dokan-sample.test/admin/modules/activate', params={
  'module': [
  "string"
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

result = RestClient.put 'http://dokan-sample.test/admin/modules/activate',
  params: {
  'module' => 'array[string]'
}, headers: headers

p JSON.parse(result)

```

`PUT /admin/modules/activate`

> Body parameter

```json
{
  "module": [
    "string"
  ]
}
```

<h3 id="put__admin_modules_activate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|module|query|array[string]|true|Basename of the module as array|
|body|body|object|true|none|
|» module|body|[string]|false|Basename of the module as array|

<h3 id="put__admin_modules_activate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__admin_modules_activate

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
    $response = $client->request('PATCH','http://dokan-sample.test/admin/modules/activate', array(
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

r = requests.patch('http://dokan-sample.test/admin/modules/activate', params={
  'module': [
  "string"
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

result = RestClient.patch 'http://dokan-sample.test/admin/modules/activate',
  params: {
  'module' => 'array[string]'
}, headers: headers

p JSON.parse(result)

```

`PATCH /admin/modules/activate`

> Body parameter

```json
{
  "module": [
    "string"
  ]
}
```

<h3 id="patch__admin_modules_activate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|module|query|array[string]|true|Basename of the module as array|
|body|body|object|true|none|
|» module|body|[string]|false|Basename of the module as array|

<h3 id="patch__admin_modules_activate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__admin_modules_deactivate

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
    $response = $client->request('POST','http://dokan-sample.test/admin/modules/deactivate', array(
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

r = requests.post('http://dokan-sample.test/admin/modules/deactivate', params={
  'module': [
  "string"
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

result = RestClient.post 'http://dokan-sample.test/admin/modules/deactivate',
  params: {
  'module' => 'array[string]'
}, headers: headers

p JSON.parse(result)

```

`POST /admin/modules/deactivate`

> Body parameter

```json
{
  "module": [
    "string"
  ]
}
```

<h3 id="post__admin_modules_deactivate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|module|query|array[string]|true|Basename of the module as array|
|body|body|object|true|none|
|» module|body|[string]|false|Basename of the module as array|

<h3 id="post__admin_modules_deactivate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__admin_modules_deactivate

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
    $response = $client->request('PUT','http://dokan-sample.test/admin/modules/deactivate', array(
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

r = requests.put('http://dokan-sample.test/admin/modules/deactivate', params={
  'module': [
  "string"
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

result = RestClient.put 'http://dokan-sample.test/admin/modules/deactivate',
  params: {
  'module' => 'array[string]'
}, headers: headers

p JSON.parse(result)

```

`PUT /admin/modules/deactivate`

> Body parameter

```json
{
  "module": [
    "string"
  ]
}
```

<h3 id="put__admin_modules_deactivate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|module|query|array[string]|true|Basename of the module as array|
|body|body|object|true|none|
|» module|body|[string]|false|Basename of the module as array|

<h3 id="put__admin_modules_deactivate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__admin_modules_deactivate

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
    $response = $client->request('PATCH','http://dokan-sample.test/admin/modules/deactivate', array(
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

r = requests.patch('http://dokan-sample.test/admin/modules/deactivate', params={
  'module': [
  "string"
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

result = RestClient.patch 'http://dokan-sample.test/admin/modules/deactivate',
  params: {
  'module' => 'array[string]'
}, headers: headers

p JSON.parse(result)

```

`PATCH /admin/modules/deactivate`

> Body parameter

```json
{
  "module": [
    "string"
  ]
}
```

<h3 id="patch__admin_modules_deactivate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|module|query|array[string]|true|Basename of the module as array|
|body|body|object|true|none|
|» module|body|[string]|false|Basename of the module as array|

<h3 id="patch__admin_modules_deactivate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

