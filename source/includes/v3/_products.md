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

## get__products

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products', array(
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

r = requests.get('http://dokan-sample.test/products')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products',
  params: {
  }

p JSON.parse(result)

```

`GET /products`

<h3 id="get__products-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|integer|false|Unique identifier for the object.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__products-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products

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
    $response = $client->request('POST','http://dokan-sample.test/products', array(
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

r = requests.post('http://dokan-sample.test/products', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products`

> Body parameter

```json
{
  "id": 0,
  "name": "string",
  "slug": "string",
  "type": "simple",
  "status": "draft",
  "featured": true,
  "catalog_visibility": "visible",
  "description": "string",
  "short_description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
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
  "external_url": "http://example.com",
  "button_text": "string",
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": true,
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "sold_individually": true,
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "reviews_allowed": true,
  "upsell_ids": [
    0
  ],
  "cross_sell_ids": [
    0
  ],
  "parent_id": 0,
  "purchase_note": "string",
  "categories": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "tags": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "images": [
    {
      "id": 0,
      "date_created": "2019-08-24T14:15:22Z",
      "date_created_gmt": "2019-08-24T14:15:22Z",
      "date_modified": "2019-08-24T14:15:22Z",
      "date_modified_gmt": "2019-08-24T14:15:22Z",
      "src": "http://example.com",
      "name": "string",
      "alt": "string",
      "position": 0
    }
  ],
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "position": 0,
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ],
  "default_attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "grouped_products": [
    0
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

<h3 id="post__products-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|integer|false|Unique identifier for the object.|
|name|query|string|false|Product name.|
|slug|query|string|false|Product slug.|
|type|query|string|false|Product type.|
|status|query|string|false|Product status (post status).|
|featured|query|boolean|false|Featured product.|
|catalog_visibility|query|string|false|Catalog visibility.|
|description|query|string|false|Product description.|
|short_description|query|string|false|Product short description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Product regular price.|
|sale_price|query|string|false|Product sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|virtual|query|boolean|false|If the product is virtual.|
|downloadable|query|boolean|false|If the product is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|external_url|query|string(uri)|false|Product external URL. Only for external products.|
|button_text|query|string|false|Product external button text. Only for external products.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|boolean|false|Stock management at product level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|sold_individually|query|boolean|false|Allow one item to be bought in a single order.|
|weight|query|string|false|Product weight (kg).|
|dimensions|query|object|false|Product dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|reviews_allowed|query|boolean|false|Allow reviews.|
|upsell_ids|query|array[integer]|false|List of up-sell products IDs.|
|cross_sell_ids|query|array[integer]|false|List of cross-sell products IDs.|
|parent_id|query|integer|false|Product parent ID.|
|purchase_note|query|string|false|Optional note to send the customer after purchase.|
|categories|query|array[object]|false|List of categories.|
|tags|query|array[object]|false|List of tags.|
|images|query|array[object]|false|List of images.|
|attributes|query|array[object]|false|List of attributes.|
|default_attributes|query|array[object]|false|Defaults variation attributes.|
|grouped_products|query|array[integer]|false|List of grouped products ID.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» id|body|integer|false|Unique identifier for the object.|
|» name|body|string|false|Product name.|
|» slug|body|string|false|Product slug.|
|» type|body|string|false|Product type.|
|» status|body|string|false|Product status (post status).|
|» featured|body|boolean|false|Featured product.|
|» catalog_visibility|body|string|false|Catalog visibility.|
|» description|body|string|false|Product description.|
|» short_description|body|string|false|Product short description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Product regular price.|
|» sale_price|body|string|false|Product sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» virtual|body|boolean|false|If the product is virtual.|
|» downloadable|body|boolean|false|If the product is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» external_url|body|string(uri)|false|Product external URL. Only for external products.|
|» button_text|body|string|false|Product external button text. Only for external products.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|boolean|false|Stock management at product level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» sold_individually|body|boolean|false|Allow one item to be bought in a single order.|
|» weight|body|string|false|Product weight (kg).|
|» dimensions|body|object|false|Product dimensions.|
|»» length|body|string|false|Product length (cm).|
|»» width|body|string|false|Product width (cm).|
|»» height|body|string|false|Product height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» reviews_allowed|body|boolean|false|Allow reviews.|
|» upsell_ids|body|[integer]|false|List of up-sell products IDs.|
|» cross_sell_ids|body|[integer]|false|List of cross-sell products IDs.|
|» parent_id|body|integer|false|Product parent ID.|
|» purchase_note|body|string|false|Optional note to send the customer after purchase.|
|» categories|body|[object]|false|List of categories.|
|»» id|body|integer|false|Category ID.|
|»» name|body|string|false|Category name.|
|»» slug|body|string|false|Category slug.|
|» tags|body|[object]|false|List of tags.|
|»» id|body|integer|false|Tag ID.|
|»» name|body|string|false|Tag name.|
|»» slug|body|string|false|Tag slug.|
|» images|body|[object]|false|List of images.|
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
|»» position|body|integer|false|Attribute position.|
|»» visible|body|boolean|false|Define if the attribute is visible on the "Additional information" tab in the product's page.|
|»» variation|body|boolean|false|Define if the attribute can be used as variation.|
|»» options|body|[string]|false|List of available term names of the attribute.|
|» default_attributes|body|[object]|false|Defaults variation attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» grouped_products|body|[integer]|false|List of grouped products ID.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|simple|
|type|grouped|
|type|external|
|type|variable|
|status|draft|
|status|pending|
|status|private|
|status|publish|
|catalog_visibility|visible|
|catalog_visibility|catalog|
|catalog_visibility|search|
|catalog_visibility|hidden|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» type|simple|
|» type|grouped|
|» type|external|
|» type|variable|
|» status|draft|
|» status|pending|
|» status|private|
|» status|publish|
|» catalog_visibility|visible|
|» catalog_visibility|catalog|
|» catalog_visibility|search|
|» catalog_visibility|hidden|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="post__products-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/{id}', array(
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

r = requests.get('http://dokan-sample.test/products/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /products/{id}`

<h3 id="get__products_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__products_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/products/{id}', array(
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

r = requests.post('http://dokan-sample.test/products/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "simple",
  "status": "draft",
  "featured": true,
  "catalog_visibility": "visible",
  "description": "string",
  "short_description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
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
  "external_url": "http://example.com",
  "button_text": "string",
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": true,
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "sold_individually": true,
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "reviews_allowed": true,
  "upsell_ids": [
    0
  ],
  "cross_sell_ids": [
    0
  ],
  "parent_id": 0,
  "purchase_note": "string",
  "categories": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "tags": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "images": [
    {
      "id": 0,
      "date_created": "2019-08-24T14:15:22Z",
      "date_created_gmt": "2019-08-24T14:15:22Z",
      "date_modified": "2019-08-24T14:15:22Z",
      "date_modified_gmt": "2019-08-24T14:15:22Z",
      "src": "http://example.com",
      "name": "string",
      "alt": "string",
      "position": 0
    }
  ],
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "position": 0,
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ],
  "default_attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "grouped_products": [
    0
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

<h3 id="post__products_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|name|query|string|false|Product name.|
|slug|query|string|false|Product slug.|
|type|query|string|false|Product type.|
|status|query|string|false|Product status (post status).|
|featured|query|boolean|false|Featured product.|
|catalog_visibility|query|string|false|Catalog visibility.|
|description|query|string|false|Product description.|
|short_description|query|string|false|Product short description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Product regular price.|
|sale_price|query|string|false|Product sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|virtual|query|boolean|false|If the product is virtual.|
|downloadable|query|boolean|false|If the product is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|external_url|query|string(uri)|false|Product external URL. Only for external products.|
|button_text|query|string|false|Product external button text. Only for external products.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|boolean|false|Stock management at product level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|sold_individually|query|boolean|false|Allow one item to be bought in a single order.|
|weight|query|string|false|Product weight (kg).|
|dimensions|query|object|false|Product dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|reviews_allowed|query|boolean|false|Allow reviews.|
|upsell_ids|query|array[integer]|false|List of up-sell products IDs.|
|cross_sell_ids|query|array[integer]|false|List of cross-sell products IDs.|
|parent_id|query|integer|false|Product parent ID.|
|purchase_note|query|string|false|Optional note to send the customer after purchase.|
|categories|query|array[object]|false|List of categories.|
|tags|query|array[object]|false|List of tags.|
|images|query|array[object]|false|List of images.|
|attributes|query|array[object]|false|List of attributes.|
|default_attributes|query|array[object]|false|Defaults variation attributes.|
|grouped_products|query|array[integer]|false|List of grouped products ID.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» name|body|string|false|Product name.|
|» slug|body|string|false|Product slug.|
|» type|body|string|false|Product type.|
|» status|body|string|false|Product status (post status).|
|» featured|body|boolean|false|Featured product.|
|» catalog_visibility|body|string|false|Catalog visibility.|
|» description|body|string|false|Product description.|
|» short_description|body|string|false|Product short description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Product regular price.|
|» sale_price|body|string|false|Product sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» virtual|body|boolean|false|If the product is virtual.|
|» downloadable|body|boolean|false|If the product is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» external_url|body|string(uri)|false|Product external URL. Only for external products.|
|» button_text|body|string|false|Product external button text. Only for external products.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|boolean|false|Stock management at product level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» sold_individually|body|boolean|false|Allow one item to be bought in a single order.|
|» weight|body|string|false|Product weight (kg).|
|» dimensions|body|object|false|Product dimensions.|
|»» length|body|string|false|Product length (cm).|
|»» width|body|string|false|Product width (cm).|
|»» height|body|string|false|Product height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» reviews_allowed|body|boolean|false|Allow reviews.|
|» upsell_ids|body|[integer]|false|List of up-sell products IDs.|
|» cross_sell_ids|body|[integer]|false|List of cross-sell products IDs.|
|» parent_id|body|integer|false|Product parent ID.|
|» purchase_note|body|string|false|Optional note to send the customer after purchase.|
|» categories|body|[object]|false|List of categories.|
|»» id|body|integer|false|Category ID.|
|»» name|body|string|false|Category name.|
|»» slug|body|string|false|Category slug.|
|» tags|body|[object]|false|List of tags.|
|»» id|body|integer|false|Tag ID.|
|»» name|body|string|false|Tag name.|
|»» slug|body|string|false|Tag slug.|
|» images|body|[object]|false|List of images.|
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
|»» position|body|integer|false|Attribute position.|
|»» visible|body|boolean|false|Define if the attribute is visible on the "Additional information" tab in the product's page.|
|»» variation|body|boolean|false|Define if the attribute can be used as variation.|
|»» options|body|[string]|false|List of available term names of the attribute.|
|» default_attributes|body|[object]|false|Defaults variation attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» grouped_products|body|[integer]|false|List of grouped products ID.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|simple|
|type|grouped|
|type|external|
|type|variable|
|status|draft|
|status|pending|
|status|private|
|status|publish|
|catalog_visibility|visible|
|catalog_visibility|catalog|
|catalog_visibility|search|
|catalog_visibility|hidden|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» type|simple|
|» type|grouped|
|» type|external|
|» type|variable|
|» status|draft|
|» status|pending|
|» status|private|
|» status|publish|
|» catalog_visibility|visible|
|» catalog_visibility|catalog|
|» catalog_visibility|search|
|» catalog_visibility|hidden|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="post__products_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/products/{id}', array(
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

r = requests.put('http://dokan-sample.test/products/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/products/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /products/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "simple",
  "status": "draft",
  "featured": true,
  "catalog_visibility": "visible",
  "description": "string",
  "short_description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
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
  "external_url": "http://example.com",
  "button_text": "string",
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": true,
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "sold_individually": true,
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "reviews_allowed": true,
  "upsell_ids": [
    0
  ],
  "cross_sell_ids": [
    0
  ],
  "parent_id": 0,
  "purchase_note": "string",
  "categories": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "tags": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "images": [
    {
      "id": 0,
      "date_created": "2019-08-24T14:15:22Z",
      "date_created_gmt": "2019-08-24T14:15:22Z",
      "date_modified": "2019-08-24T14:15:22Z",
      "date_modified_gmt": "2019-08-24T14:15:22Z",
      "src": "http://example.com",
      "name": "string",
      "alt": "string",
      "position": 0
    }
  ],
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "position": 0,
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ],
  "default_attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "grouped_products": [
    0
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

<h3 id="put__products_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|name|query|string|false|Product name.|
|slug|query|string|false|Product slug.|
|type|query|string|false|Product type.|
|status|query|string|false|Product status (post status).|
|featured|query|boolean|false|Featured product.|
|catalog_visibility|query|string|false|Catalog visibility.|
|description|query|string|false|Product description.|
|short_description|query|string|false|Product short description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Product regular price.|
|sale_price|query|string|false|Product sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|virtual|query|boolean|false|If the product is virtual.|
|downloadable|query|boolean|false|If the product is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|external_url|query|string(uri)|false|Product external URL. Only for external products.|
|button_text|query|string|false|Product external button text. Only for external products.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|boolean|false|Stock management at product level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|sold_individually|query|boolean|false|Allow one item to be bought in a single order.|
|weight|query|string|false|Product weight (kg).|
|dimensions|query|object|false|Product dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|reviews_allowed|query|boolean|false|Allow reviews.|
|upsell_ids|query|array[integer]|false|List of up-sell products IDs.|
|cross_sell_ids|query|array[integer]|false|List of cross-sell products IDs.|
|parent_id|query|integer|false|Product parent ID.|
|purchase_note|query|string|false|Optional note to send the customer after purchase.|
|categories|query|array[object]|false|List of categories.|
|tags|query|array[object]|false|List of tags.|
|images|query|array[object]|false|List of images.|
|attributes|query|array[object]|false|List of attributes.|
|default_attributes|query|array[object]|false|Defaults variation attributes.|
|grouped_products|query|array[integer]|false|List of grouped products ID.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» name|body|string|false|Product name.|
|» slug|body|string|false|Product slug.|
|» type|body|string|false|Product type.|
|» status|body|string|false|Product status (post status).|
|» featured|body|boolean|false|Featured product.|
|» catalog_visibility|body|string|false|Catalog visibility.|
|» description|body|string|false|Product description.|
|» short_description|body|string|false|Product short description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Product regular price.|
|» sale_price|body|string|false|Product sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» virtual|body|boolean|false|If the product is virtual.|
|» downloadable|body|boolean|false|If the product is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» external_url|body|string(uri)|false|Product external URL. Only for external products.|
|» button_text|body|string|false|Product external button text. Only for external products.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|boolean|false|Stock management at product level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» sold_individually|body|boolean|false|Allow one item to be bought in a single order.|
|» weight|body|string|false|Product weight (kg).|
|» dimensions|body|object|false|Product dimensions.|
|»» length|body|string|false|Product length (cm).|
|»» width|body|string|false|Product width (cm).|
|»» height|body|string|false|Product height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» reviews_allowed|body|boolean|false|Allow reviews.|
|» upsell_ids|body|[integer]|false|List of up-sell products IDs.|
|» cross_sell_ids|body|[integer]|false|List of cross-sell products IDs.|
|» parent_id|body|integer|false|Product parent ID.|
|» purchase_note|body|string|false|Optional note to send the customer after purchase.|
|» categories|body|[object]|false|List of categories.|
|»» id|body|integer|false|Category ID.|
|»» name|body|string|false|Category name.|
|»» slug|body|string|false|Category slug.|
|» tags|body|[object]|false|List of tags.|
|»» id|body|integer|false|Tag ID.|
|»» name|body|string|false|Tag name.|
|»» slug|body|string|false|Tag slug.|
|» images|body|[object]|false|List of images.|
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
|»» position|body|integer|false|Attribute position.|
|»» visible|body|boolean|false|Define if the attribute is visible on the "Additional information" tab in the product's page.|
|»» variation|body|boolean|false|Define if the attribute can be used as variation.|
|»» options|body|[string]|false|List of available term names of the attribute.|
|» default_attributes|body|[object]|false|Defaults variation attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» grouped_products|body|[integer]|false|List of grouped products ID.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|simple|
|type|grouped|
|type|external|
|type|variable|
|status|draft|
|status|pending|
|status|private|
|status|publish|
|catalog_visibility|visible|
|catalog_visibility|catalog|
|catalog_visibility|search|
|catalog_visibility|hidden|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» type|simple|
|» type|grouped|
|» type|external|
|» type|variable|
|» status|draft|
|» status|pending|
|» status|private|
|» status|publish|
|» catalog_visibility|visible|
|» catalog_visibility|catalog|
|» catalog_visibility|search|
|» catalog_visibility|hidden|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="put__products_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/{id}', array(
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

r = requests.patch('http://dokan-sample.test/products/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/products/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /products/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "simple",
  "status": "draft",
  "featured": true,
  "catalog_visibility": "visible",
  "description": "string",
  "short_description": "string",
  "sku": "string",
  "regular_price": "string",
  "sale_price": "string",
  "date_on_sale_from": "2019-08-24T14:15:22Z",
  "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
  "date_on_sale_to": "2019-08-24T14:15:22Z",
  "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
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
  "external_url": "http://example.com",
  "button_text": "string",
  "tax_status": "taxable",
  "tax_class": "string",
  "manage_stock": true,
  "stock_quantity": 0,
  "in_stock": true,
  "backorders": "no",
  "sold_individually": true,
  "weight": "string",
  "dimensions": {
    "length": "string",
    "width": "string",
    "height": "string"
  },
  "shipping_class": "string",
  "reviews_allowed": true,
  "upsell_ids": [
    0
  ],
  "cross_sell_ids": [
    0
  ],
  "parent_id": 0,
  "purchase_note": "string",
  "categories": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "tags": [
    {
      "id": 0,
      "name": "string",
      "slug": "string"
    }
  ],
  "images": [
    {
      "id": 0,
      "date_created": "2019-08-24T14:15:22Z",
      "date_created_gmt": "2019-08-24T14:15:22Z",
      "date_modified": "2019-08-24T14:15:22Z",
      "date_modified_gmt": "2019-08-24T14:15:22Z",
      "src": "http://example.com",
      "name": "string",
      "alt": "string",
      "position": 0
    }
  ],
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "position": 0,
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ],
  "default_attributes": [
    {
      "id": 0,
      "name": "string",
      "option": "string"
    }
  ],
  "grouped_products": [
    0
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

<h3 id="patch__products_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|name|query|string|false|Product name.|
|slug|query|string|false|Product slug.|
|type|query|string|false|Product type.|
|status|query|string|false|Product status (post status).|
|featured|query|boolean|false|Featured product.|
|catalog_visibility|query|string|false|Catalog visibility.|
|description|query|string|false|Product description.|
|short_description|query|string|false|Product short description.|
|sku|query|string|false|Unique identifier.|
|regular_price|query|string|false|Product regular price.|
|sale_price|query|string|false|Product sale price.|
|date_on_sale_from|query|string(date-time)|false|Start date of sale price, in the site's timezone.|
|date_on_sale_from_gmt|query|string(date-time)|false|Start date of sale price, as GMT.|
|date_on_sale_to|query|string(date-time)|false|End date of sale price, in the site's timezone.|
|date_on_sale_to_gmt|query|string(date-time)|false|End date of sale price, as GMT.|
|virtual|query|boolean|false|If the product is virtual.|
|downloadable|query|boolean|false|If the product is downloadable.|
|downloads|query|array[object]|false|List of downloadable files.|
|download_limit|query|integer|false|Number of times downloadable files can be downloaded after purchase.|
|download_expiry|query|integer|false|Number of days until access to downloadable files expires.|
|external_url|query|string(uri)|false|Product external URL. Only for external products.|
|button_text|query|string|false|Product external button text. Only for external products.|
|tax_status|query|string|false|Tax status.|
|tax_class|query|string|false|Tax class.|
|manage_stock|query|boolean|false|Stock management at product level.|
|stock_quantity|query|integer|false|Stock quantity.|
|in_stock|query|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|backorders|query|string|false|If managing stock, this controls if backorders are allowed.|
|sold_individually|query|boolean|false|Allow one item to be bought in a single order.|
|weight|query|string|false|Product weight (kg).|
|dimensions|query|object|false|Product dimensions.|
|shipping_class|query|string|false|Shipping class slug.|
|reviews_allowed|query|boolean|false|Allow reviews.|
|upsell_ids|query|array[integer]|false|List of up-sell products IDs.|
|cross_sell_ids|query|array[integer]|false|List of cross-sell products IDs.|
|parent_id|query|integer|false|Product parent ID.|
|purchase_note|query|string|false|Optional note to send the customer after purchase.|
|categories|query|array[object]|false|List of categories.|
|tags|query|array[object]|false|List of tags.|
|images|query|array[object]|false|List of images.|
|attributes|query|array[object]|false|List of attributes.|
|default_attributes|query|array[object]|false|Defaults variation attributes.|
|grouped_products|query|array[integer]|false|List of grouped products ID.|
|menu_order|query|integer|false|Menu order, used to custom sort products.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» name|body|string|false|Product name.|
|» slug|body|string|false|Product slug.|
|» type|body|string|false|Product type.|
|» status|body|string|false|Product status (post status).|
|» featured|body|boolean|false|Featured product.|
|» catalog_visibility|body|string|false|Catalog visibility.|
|» description|body|string|false|Product description.|
|» short_description|body|string|false|Product short description.|
|» sku|body|string|false|Unique identifier.|
|» regular_price|body|string|false|Product regular price.|
|» sale_price|body|string|false|Product sale price.|
|» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|» virtual|body|boolean|false|If the product is virtual.|
|» downloadable|body|boolean|false|If the product is downloadable.|
|» downloads|body|[object]|false|List of downloadable files.|
|»» id|body|string|false|File MD5 hash.|
|»» name|body|string|false|File name.|
|»» file|body|string|false|File URL.|
|» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|» external_url|body|string(uri)|false|Product external URL. Only for external products.|
|» button_text|body|string|false|Product external button text. Only for external products.|
|» tax_status|body|string|false|Tax status.|
|» tax_class|body|string|false|Tax class.|
|» manage_stock|body|boolean|false|Stock management at product level.|
|» stock_quantity|body|integer|false|Stock quantity.|
|» in_stock|body|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|» sold_individually|body|boolean|false|Allow one item to be bought in a single order.|
|» weight|body|string|false|Product weight (kg).|
|» dimensions|body|object|false|Product dimensions.|
|»» length|body|string|false|Product length (cm).|
|»» width|body|string|false|Product width (cm).|
|»» height|body|string|false|Product height (cm).|
|» shipping_class|body|string|false|Shipping class slug.|
|» reviews_allowed|body|boolean|false|Allow reviews.|
|» upsell_ids|body|[integer]|false|List of up-sell products IDs.|
|» cross_sell_ids|body|[integer]|false|List of cross-sell products IDs.|
|» parent_id|body|integer|false|Product parent ID.|
|» purchase_note|body|string|false|Optional note to send the customer after purchase.|
|» categories|body|[object]|false|List of categories.|
|»» id|body|integer|false|Category ID.|
|»» name|body|string|false|Category name.|
|»» slug|body|string|false|Category slug.|
|» tags|body|[object]|false|List of tags.|
|»» id|body|integer|false|Tag ID.|
|»» name|body|string|false|Tag name.|
|»» slug|body|string|false|Tag slug.|
|» images|body|[object]|false|List of images.|
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
|»» position|body|integer|false|Attribute position.|
|»» visible|body|boolean|false|Define if the attribute is visible on the "Additional information" tab in the product's page.|
|»» variation|body|boolean|false|Define if the attribute can be used as variation.|
|»» options|body|[string]|false|List of available term names of the attribute.|
|» default_attributes|body|[object]|false|Defaults variation attributes.|
|»» id|body|integer|false|Attribute ID.|
|»» name|body|string|false|Attribute name.|
|»» option|body|string|false|Selected attribute term name.|
|» grouped_products|body|[integer]|false|List of grouped products ID.|
|» menu_order|body|integer|false|Menu order, used to custom sort products.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|string|false|Meta value.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|simple|
|type|grouped|
|type|external|
|type|variable|
|status|draft|
|status|pending|
|status|private|
|status|publish|
|catalog_visibility|visible|
|catalog_visibility|catalog|
|catalog_visibility|search|
|catalog_visibility|hidden|
|tax_status|taxable|
|tax_status|shipping|
|tax_status|none|
|backorders|no|
|backorders|notify|
|backorders|yes|
|» type|simple|
|» type|grouped|
|» type|external|
|» type|variable|
|» status|draft|
|» status|pending|
|» status|private|
|» status|publish|
|» catalog_visibility|visible|
|» catalog_visibility|catalog|
|» catalog_visibility|search|
|» catalog_visibility|hidden|
|» tax_status|taxable|
|» tax_status|shipping|
|» tax_status|none|
|» backorders|no|
|» backorders|notify|
|» backorders|yes|

<h3 id="patch__products_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__products_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/products/{id}', array(
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

r = requests.delete('http://dokan-sample.test/products/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/products/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /products/{id}`

<h3 id="delete__products_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|force|query|boolean|false|Whether to bypass trash and force deletion.|

<h3 id="delete__products_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_summary

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/summary', array(
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

r = requests.get('http://dokan-sample.test/products/summary')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/summary',
  params: {
  }

p JSON.parse(result)

```

`GET /products/summary`

<h3 id="get__products_summary-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_{id}_related

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/{id}/related', array(
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

r = requests.get('http://dokan-sample.test/products/{id}/related')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/{id}/related',
  params: {
  }

p JSON.parse(result)

```

`GET /products/{id}/related`

<h3 id="get__products_{id}_related-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|per_page|query|integer|false|Number of product you want to get top rated product|

<h3 id="get__products_{id}_related-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_top_rated

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/top_rated', array(
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

r = requests.get('http://dokan-sample.test/products/top_rated')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/top_rated',
  params: {
  }

p JSON.parse(result)

```

`GET /products/top_rated`

<h3 id="get__products_top_rated-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|per_page|query|integer|false|Number of product you want to get top rated product|
|page|query|integer|false|Number of page number|
|seller_id|query|integer|false|Top rated product for specific vendor|

<h3 id="get__products_top_rated-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_best_selling

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/best_selling', array(
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

r = requests.get('http://dokan-sample.test/products/best_selling')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/best_selling',
  params: {
  }

p JSON.parse(result)

```

`GET /products/best_selling`

<h3 id="get__products_best_selling-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|per_page|query|integer|false|Number of product you want to get top rated product|
|page|query|integer|false|Number of page number|
|seller_id|query|integer|false|Top rated product for specific vendor|

<h3 id="get__products_best_selling-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_featured

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/featured', array(
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

r = requests.get('http://dokan-sample.test/products/featured')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/featured',
  params: {
  }

p JSON.parse(result)

```

`GET /products/featured`

<h3 id="get__products_featured-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|per_page|query|integer|false|Number of product you want to get top rated product|
|page|query|integer|false|Number of page number|
|seller_id|query|integer|false|Top rated product for specific vendor|

<h3 id="get__products_featured-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_latest

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/latest', array(
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

r = requests.get('http://dokan-sample.test/products/latest')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/latest',
  params: {
  }

p JSON.parse(result)

```

`GET /products/latest`

<h3 id="get__products_latest-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|per_page|query|integer|false|Number of product you want to get top rated product|
|page|query|integer|false|Number of page number|
|seller_id|query|integer|false|Top rated product for specific vendor|

<h3 id="get__products_latest-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_multistep-categories

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/multistep-categories', array(
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

r = requests.get('http://dokan-sample.test/products/multistep-categories')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/multistep-categories',
  params: {
  }

p JSON.parse(result)

```

`GET /products/multistep-categories`

<h3 id="get__products_multistep-categories-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_attributes

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/attributes', array(
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

r = requests.get('http://dokan-sample.test/products/attributes')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/attributes',
  params: {
  }

p JSON.parse(result)

```

`GET /products/attributes`

<h3 id="get__products_attributes-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__products_attributes-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes', array(
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

r = requests.post('http://dokan-sample.test/products/attributes', params={
  'name': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/attributes',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /products/attributes`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "select",
  "order_by": "menu_order",
  "has_archives": true
}
```

<h3 id="post__products_attributes-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|true|Name for the resource.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|type|query|string|false|Type of attribute.|
|order_by|query|string|false|Default sort order.|
|has_archives|query|boolean|false|Enable/Disable attribute archives.|
|body|body|object|true|none|
|» name|body|string|false|Name for the resource.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» type|body|string|false|Type of attribute.|
|» order_by|body|string|false|Default sort order.|
|» has_archives|body|boolean|false|Enable/Disable attribute archives.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|select|
|order_by|menu_order|
|order_by|name|
|order_by|name_num|
|order_by|id|
|» type|select|
|» order_by|menu_order|
|» order_by|name|
|» order_by|name_num|
|» order_by|id|

<h3 id="post__products_attributes-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_attributes_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/attributes/{id}', array(
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

r = requests.get('http://dokan-sample.test/products/attributes/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/attributes/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /products/attributes/{id}`

<h3 id="get__products_attributes_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__products_attributes_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes/{id}', array(
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

r = requests.post('http://dokan-sample.test/products/attributes/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/attributes/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/attributes/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "select",
  "order_by": "menu_order",
  "has_archives": true
}
```

<h3 id="post__products_attributes_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|name|query|string|false|Attribute name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|type|query|string|false|Type of attribute.|
|order_by|query|string|false|Default sort order.|
|has_archives|query|boolean|false|Enable/Disable attribute archives.|
|body|body|object|true|none|
|» name|body|string|false|Attribute name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» type|body|string|false|Type of attribute.|
|» order_by|body|string|false|Default sort order.|
|» has_archives|body|boolean|false|Enable/Disable attribute archives.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|select|
|order_by|menu_order|
|order_by|name|
|order_by|name_num|
|order_by|id|
|» type|select|
|» order_by|menu_order|
|» order_by|name|
|» order_by|name_num|
|» order_by|id|

<h3 id="post__products_attributes_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_attributes_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/products/attributes/{id}', array(
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

r = requests.put('http://dokan-sample.test/products/attributes/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/products/attributes/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /products/attributes/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "select",
  "order_by": "menu_order",
  "has_archives": true
}
```

<h3 id="put__products_attributes_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|name|query|string|false|Attribute name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|type|query|string|false|Type of attribute.|
|order_by|query|string|false|Default sort order.|
|has_archives|query|boolean|false|Enable/Disable attribute archives.|
|body|body|object|true|none|
|» name|body|string|false|Attribute name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» type|body|string|false|Type of attribute.|
|» order_by|body|string|false|Default sort order.|
|» has_archives|body|boolean|false|Enable/Disable attribute archives.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|select|
|order_by|menu_order|
|order_by|name|
|order_by|name_num|
|order_by|id|
|» type|select|
|» order_by|menu_order|
|» order_by|name|
|» order_by|name_num|
|» order_by|id|

<h3 id="put__products_attributes_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_attributes_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/attributes/{id}', array(
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

r = requests.patch('http://dokan-sample.test/products/attributes/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/products/attributes/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /products/attributes/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "select",
  "order_by": "menu_order",
  "has_archives": true
}
```

<h3 id="patch__products_attributes_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|name|query|string|false|Attribute name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|type|query|string|false|Type of attribute.|
|order_by|query|string|false|Default sort order.|
|has_archives|query|boolean|false|Enable/Disable attribute archives.|
|body|body|object|true|none|
|» name|body|string|false|Attribute name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» type|body|string|false|Type of attribute.|
|» order_by|body|string|false|Default sort order.|
|» has_archives|body|boolean|false|Enable/Disable attribute archives.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|select|
|order_by|menu_order|
|order_by|name|
|order_by|name_num|
|order_by|id|
|» type|select|
|» order_by|menu_order|
|» order_by|name|
|» order_by|name_num|
|» order_by|id|

<h3 id="patch__products_attributes_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__products_attributes_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/products/attributes/{id}', array(
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

r = requests.delete('http://dokan-sample.test/products/attributes/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/products/attributes/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /products/attributes/{id}`

<h3 id="delete__products_attributes_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|force|query|boolean|false|Required to be true, as resource does not support trashing.|

<h3 id="delete__products_attributes_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes_batch

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes/batch', array(
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

r = requests.post('http://dokan-sample.test/products/attributes/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/attributes/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/attributes/batch`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "select",
  "order_by": "menu_order",
  "has_archives": true
}
```

<h3 id="post__products_attributes_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|false|Attribute name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|type|query|string|false|Type of attribute.|
|order_by|query|string|false|Default sort order.|
|has_archives|query|boolean|false|Enable/Disable attribute archives.|
|body|body|object|true|none|
|» name|body|string|false|Attribute name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» type|body|string|false|Type of attribute.|
|» order_by|body|string|false|Default sort order.|
|» has_archives|body|boolean|false|Enable/Disable attribute archives.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|select|
|order_by|menu_order|
|order_by|name|
|order_by|name_num|
|order_by|id|
|» type|select|
|» order_by|menu_order|
|» order_by|name|
|» order_by|name_num|
|» order_by|id|

<h3 id="post__products_attributes_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_attributes_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/products/attributes/batch', array(
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

r = requests.put('http://dokan-sample.test/products/attributes/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/products/attributes/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /products/attributes/batch`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "select",
  "order_by": "menu_order",
  "has_archives": true
}
```

<h3 id="put__products_attributes_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|false|Attribute name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|type|query|string|false|Type of attribute.|
|order_by|query|string|false|Default sort order.|
|has_archives|query|boolean|false|Enable/Disable attribute archives.|
|body|body|object|true|none|
|» name|body|string|false|Attribute name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» type|body|string|false|Type of attribute.|
|» order_by|body|string|false|Default sort order.|
|» has_archives|body|boolean|false|Enable/Disable attribute archives.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|select|
|order_by|menu_order|
|order_by|name|
|order_by|name_num|
|order_by|id|
|» type|select|
|» order_by|menu_order|
|» order_by|name|
|» order_by|name_num|
|» order_by|id|

<h3 id="put__products_attributes_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_attributes_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/attributes/batch', array(
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

r = requests.patch('http://dokan-sample.test/products/attributes/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/products/attributes/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /products/attributes/batch`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "type": "select",
  "order_by": "menu_order",
  "has_archives": true
}
```

<h3 id="patch__products_attributes_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|false|Attribute name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|type|query|string|false|Type of attribute.|
|order_by|query|string|false|Default sort order.|
|has_archives|query|boolean|false|Enable/Disable attribute archives.|
|body|body|object|true|none|
|» name|body|string|false|Attribute name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» type|body|string|false|Type of attribute.|
|» order_by|body|string|false|Default sort order.|
|» has_archives|body|boolean|false|Enable/Disable attribute archives.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|select|
|order_by|menu_order|
|order_by|name|
|order_by|name_num|
|order_by|id|
|» type|select|
|» order_by|menu_order|
|» order_by|name|
|» order_by|name_num|
|» order_by|id|

<h3 id="patch__products_attributes_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes_edit-product_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes/edit-product/{id}', array(
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

r = requests.post('http://dokan-sample.test/products/attributes/edit-product/{id}', params={
  'attributes': [
  {
    "id": 0,
    "name": "string",
    "visible": true,
    "variation": true,
    "options": [
      "string"
    ]
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

result = RestClient.post 'http://dokan-sample.test/products/attributes/edit-product/{id}',
  params: {
  'attributes' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`POST /products/attributes/edit-product/{id}`

> Body parameter

```json
{
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ]
}
```

<h3 id="post__products_attributes_edit-product_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attributes|query|array[object]|true|Attribute options.|
|body|body|object|true|none|
|» attributes|body|[object]|false|Attribute options.|
|»» id|body|integer|false|Attribute id.|
|»» name|body|string|false|Attribute name.|
|»» visible|body|boolean|false|Attribute visible in product list page or not.|
|»» variation|body|boolean|false|Attribute is for variation or not.|
|»» options|body|[string]|true|Attribute values.|

<h3 id="post__products_attributes_edit-product_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_attributes_edit-product_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/products/attributes/edit-product/{id}', array(
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

r = requests.put('http://dokan-sample.test/products/attributes/edit-product/{id}', params={
  'attributes': [
  {
    "id": 0,
    "name": "string",
    "visible": true,
    "variation": true,
    "options": [
      "string"
    ]
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

result = RestClient.put 'http://dokan-sample.test/products/attributes/edit-product/{id}',
  params: {
  'attributes' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`PUT /products/attributes/edit-product/{id}`

> Body parameter

```json
{
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ]
}
```

<h3 id="put__products_attributes_edit-product_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attributes|query|array[object]|true|Attribute options.|
|body|body|object|true|none|
|» attributes|body|[object]|false|Attribute options.|
|»» id|body|integer|false|Attribute id.|
|»» name|body|string|false|Attribute name.|
|»» visible|body|boolean|false|Attribute visible in product list page or not.|
|»» variation|body|boolean|false|Attribute is for variation or not.|
|»» options|body|[string]|true|Attribute values.|

<h3 id="put__products_attributes_edit-product_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_attributes_edit-product_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/attributes/edit-product/{id}', array(
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

r = requests.patch('http://dokan-sample.test/products/attributes/edit-product/{id}', params={
  'attributes': [
  {
    "id": 0,
    "name": "string",
    "visible": true,
    "variation": true,
    "options": [
      "string"
    ]
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

result = RestClient.patch 'http://dokan-sample.test/products/attributes/edit-product/{id}',
  params: {
  'attributes' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`PATCH /products/attributes/edit-product/{id}`

> Body parameter

```json
{
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ]
}
```

<h3 id="patch__products_attributes_edit-product_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attributes|query|array[object]|true|Attribute options.|
|body|body|object|true|none|
|» attributes|body|[object]|false|Attribute options.|
|»» id|body|integer|false|Attribute id.|
|»» name|body|string|false|Attribute name.|
|»» visible|body|boolean|false|Attribute visible in product list page or not.|
|»» variation|body|boolean|false|Attribute is for variation or not.|
|»» options|body|[string]|true|Attribute values.|

<h3 id="patch__products_attributes_edit-product_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes_set-default_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes/set-default/{id}', array(
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

r = requests.post('http://dokan-sample.test/products/attributes/set-default/{id}', params={
  'attributes': [
  {
    "id": 0,
    "name": "string",
    "visible": true,
    "variation": true,
    "options": [
      "string"
    ]
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

result = RestClient.post 'http://dokan-sample.test/products/attributes/set-default/{id}',
  params: {
  'attributes' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`POST /products/attributes/set-default/{id}`

> Body parameter

```json
{
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ]
}
```

<h3 id="post__products_attributes_set-default_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attributes|query|array[object]|true|Attribute options.|
|body|body|object|true|none|
|» attributes|body|[object]|false|Attribute options.|
|»» id|body|integer|false|Attribute id.|
|»» name|body|string|false|Attribute name.|
|»» visible|body|boolean|false|Attribute visible in product list page or not.|
|»» variation|body|boolean|false|Attribute is for variation or not.|
|»» options|body|[string]|true|Attribute values.|

<h3 id="post__products_attributes_set-default_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_attributes_set-default_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/products/attributes/set-default/{id}', array(
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

r = requests.put('http://dokan-sample.test/products/attributes/set-default/{id}', params={
  'attributes': [
  {
    "id": 0,
    "name": "string",
    "visible": true,
    "variation": true,
    "options": [
      "string"
    ]
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

result = RestClient.put 'http://dokan-sample.test/products/attributes/set-default/{id}',
  params: {
  'attributes' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`PUT /products/attributes/set-default/{id}`

> Body parameter

```json
{
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ]
}
```

<h3 id="put__products_attributes_set-default_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attributes|query|array[object]|true|Attribute options.|
|body|body|object|true|none|
|» attributes|body|[object]|false|Attribute options.|
|»» id|body|integer|false|Attribute id.|
|»» name|body|string|false|Attribute name.|
|»» visible|body|boolean|false|Attribute visible in product list page or not.|
|»» variation|body|boolean|false|Attribute is for variation or not.|
|»» options|body|[string]|true|Attribute values.|

<h3 id="put__products_attributes_set-default_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_attributes_set-default_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/attributes/set-default/{id}', array(
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

r = requests.patch('http://dokan-sample.test/products/attributes/set-default/{id}', params={
  'attributes': [
  {
    "id": 0,
    "name": "string",
    "visible": true,
    "variation": true,
    "options": [
      "string"
    ]
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

result = RestClient.patch 'http://dokan-sample.test/products/attributes/set-default/{id}',
  params: {
  'attributes' => 'array[object]'
}, headers: headers

p JSON.parse(result)

```

`PATCH /products/attributes/set-default/{id}`

> Body parameter

```json
{
  "attributes": [
    {
      "id": 0,
      "name": "string",
      "visible": true,
      "variation": true,
      "options": [
        "string"
      ]
    }
  ]
}
```

<h3 id="patch__products_attributes_set-default_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attributes|query|array[object]|true|Attribute options.|
|body|body|object|true|none|
|» attributes|body|[object]|false|Attribute options.|
|»» id|body|integer|false|Attribute id.|
|»» name|body|string|false|Attribute name.|
|»» visible|body|boolean|false|Attribute visible in product list page or not.|
|»» variation|body|boolean|false|Attribute is for variation or not.|
|»» options|body|[string]|true|Attribute values.|

<h3 id="patch__products_attributes_set-default_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_attributes_{attribute_id}_terms

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/attributes/{attribute_id}/terms', array(
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

r = requests.get('http://dokan-sample.test/products/attributes/{attribute_id}/terms')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/attributes/{attribute_id}/terms',
  params: {
  }

p JSON.parse(result)

```

`GET /products/attributes/{attribute_id}/terms`

<h3 id="get__products_attributes_{attribute_id}_terms-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|exclude|query|array[integer]|false|Ensure result set excludes specific IDs.|
|include|query|array[integer]|false|Limit result set to specific ids.|
|offset|query|integer|false|Offset the result set by a specific number of items. Applies to hierarchical taxonomies only.|
|order|query|string|false|Order sort attribute ascending or descending.|
|orderby|query|string|false|Sort collection by resource attribute.|
|hide_empty|query|boolean|false|Whether to hide resources not assigned to any products.|
|parent|query|integer|false|Limit result set to resources assigned to a specific parent. Applies to hierarchical taxonomies only.|
|product|query|integer|false|Limit result set to resources assigned to a specific product.|
|slug|query|string|false|Limit result set to resources with a specific slug.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|order|asc|
|order|desc|
|orderby|id|
|orderby|include|
|orderby|name|
|orderby|slug|
|orderby|term_group|
|orderby|description|
|orderby|count|

<h3 id="get__products_attributes_{attribute_id}_terms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes_{attribute_id}_terms

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes/{attribute_id}/terms', array(
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

r = requests.post('http://dokan-sample.test/products/attributes/{attribute_id}/terms', params={
  'name': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/attributes/{attribute_id}/terms',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /products/attributes/{attribute_id}/terms`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "menu_order": 0
}
```

<h3 id="post__products_attributes_{attribute_id}_terms-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|name|query|string|true|Name for the resource.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|description|query|string|false|HTML description of the resource.|
|menu_order|query|integer|false|Menu order, used to custom sort the resource.|
|body|body|object|true|none|
|» name|body|string|false|Name for the resource.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» description|body|string|false|HTML description of the resource.|
|» menu_order|body|integer|false|Menu order, used to custom sort the resource.|

<h3 id="post__products_attributes_{attribute_id}_terms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__products_attributes_{attribute_id}_terms_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', array(
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

r = requests.get('http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /products/attributes/{attribute_id}/terms/{id}`

<h3 id="get__products_attributes_{attribute_id}_terms_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__products_attributes_{attribute_id}_terms_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes_{attribute_id}_terms_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', array(
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

r = requests.post('http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/attributes/{attribute_id}/terms/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "menu_order": 0
}
```

<h3 id="post__products_attributes_{attribute_id}_terms_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|name|query|string|false|Term name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|description|query|string|false|HTML description of the resource.|
|menu_order|query|integer|false|Menu order, used to custom sort the resource.|
|body|body|object|true|none|
|» name|body|string|false|Term name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» description|body|string|false|HTML description of the resource.|
|» menu_order|body|integer|false|Menu order, used to custom sort the resource.|

<h3 id="post__products_attributes_{attribute_id}_terms_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_attributes_{attribute_id}_terms_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', array(
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

r = requests.put('http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /products/attributes/{attribute_id}/terms/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "menu_order": 0
}
```

<h3 id="put__products_attributes_{attribute_id}_terms_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|name|query|string|false|Term name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|description|query|string|false|HTML description of the resource.|
|menu_order|query|integer|false|Menu order, used to custom sort the resource.|
|body|body|object|true|none|
|» name|body|string|false|Term name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» description|body|string|false|HTML description of the resource.|
|» menu_order|body|integer|false|Menu order, used to custom sort the resource.|

<h3 id="put__products_attributes_{attribute_id}_terms_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_attributes_{attribute_id}_terms_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', array(
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

r = requests.patch('http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /products/attributes/{attribute_id}/terms/{id}`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "menu_order": 0
}
```

<h3 id="patch__products_attributes_{attribute_id}_terms_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|name|query|string|false|Term name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|description|query|string|false|HTML description of the resource.|
|menu_order|query|integer|false|Menu order, used to custom sort the resource.|
|body|body|object|true|none|
|» name|body|string|false|Term name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» description|body|string|false|HTML description of the resource.|
|» menu_order|body|integer|false|Menu order, used to custom sort the resource.|

<h3 id="patch__products_attributes_{attribute_id}_terms_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__products_attributes_{attribute_id}_terms_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}', array(
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

r = requests.delete('http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /products/attributes/{attribute_id}/terms/{id}`

<h3 id="delete__products_attributes_{attribute_id}_terms_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|force|query|boolean|false|Required to be true, as resource does not support trashing.|

<h3 id="delete__products_attributes_{attribute_id}_terms_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__products_attributes_{attribute_id}_terms_batch

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
    $response = $client->request('POST','http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch', array(
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

r = requests.post('http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /products/attributes/{attribute_id}/terms/batch`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "menu_order": 0
}
```

<h3 id="post__products_attributes_{attribute_id}_terms_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|name|query|string|false|Term name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|description|query|string|false|HTML description of the resource.|
|menu_order|query|integer|false|Menu order, used to custom sort the resource.|
|body|body|object|true|none|
|» name|body|string|false|Term name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» description|body|string|false|HTML description of the resource.|
|» menu_order|body|integer|false|Menu order, used to custom sort the resource.|

<h3 id="post__products_attributes_{attribute_id}_terms_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__products_attributes_{attribute_id}_terms_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch', array(
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

r = requests.put('http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /products/attributes/{attribute_id}/terms/batch`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "menu_order": 0
}
```

<h3 id="put__products_attributes_{attribute_id}_terms_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|name|query|string|false|Term name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|description|query|string|false|HTML description of the resource.|
|menu_order|query|integer|false|Menu order, used to custom sort the resource.|
|body|body|object|true|none|
|» name|body|string|false|Term name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» description|body|string|false|HTML description of the resource.|
|» menu_order|body|integer|false|Menu order, used to custom sort the resource.|

<h3 id="put__products_attributes_{attribute_id}_terms_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__products_attributes_{attribute_id}_terms_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch', array(
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

r = requests.patch('http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/products/attributes/{attribute_id}/terms/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /products/attributes/{attribute_id}/terms/batch`

> Body parameter

```json
{
  "name": "string",
  "slug": "string",
  "description": "string",
  "menu_order": 0
}
```

<h3 id="patch__products_attributes_{attribute_id}_terms_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|attribute_id|path|integer|true|Unique identifier for the attribute of the terms.|
|name|query|string|false|Term name.|
|slug|query|string|false|An alphanumeric identifier for the resource unique to its type.|
|description|query|string|false|HTML description of the resource.|
|menu_order|query|integer|false|Menu order, used to custom sort the resource.|
|body|body|object|true|none|
|» name|body|string|false|Term name.|
|» slug|body|string|false|An alphanumeric identifier for the resource unique to its type.|
|» description|body|string|false|HTML description of the resource.|
|» menu_order|body|integer|false|Menu order, used to custom sort the resource.|

<h3 id="patch__products_attributes_{attribute_id}_terms_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

