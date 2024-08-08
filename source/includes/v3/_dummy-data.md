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

## get__dummy-data_status

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/dummy-data/status', array(
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

r = requests.get('http://dokan-sample.test/dummy-data/status')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/dummy-data/status',
  params: {
  }

p JSON.parse(result)

```

`GET /dummy-data/status`

<h3 id="get__dummy-data_status-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__dummy-data_import

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
    $response = $client->request('POST','http://dokan-sample.test/dummy-data/import', array(
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

r = requests.post('http://dokan-sample.test/dummy-data/import', params={
  'vendor_products': [
  {
    "id": 0,
    "name": "string",
    "slug": "string",
    "permalink": "http://example.com",
    "date_created": "2019-08-24T14:15:22Z",
    "date_created_gmt": "2019-08-24T14:15:22Z",
    "date_modified": "2019-08-24T14:15:22Z",
    "date_modified_gmt": "2019-08-24T14:15:22Z",
    "type": "simple",
    "status": "draft",
    "featured": true,
    "catalog_visibility": "visible",
    "description": "string",
    "short_description": "string",
    "sku": "string",
    "price": "string",
    "regular_price": "string",
    "sale_price": "string",
    "date_on_sale_from": "2019-08-24T14:15:22Z",
    "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
    "date_on_sale_to": "2019-08-24T14:15:22Z",
    "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
    "on_sale": true,
    "purchasable": true,
    "total_sales": "string",
    "virtual": "string",
    "downloadable": "string",
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
    "stock_quantity": "string",
    "in_stock": true,
    "backorders": "no",
    "backorders_allowed": true,
    "backordered": true,
    "sold_individually": "string",
    "weight": "string",
    "dimensions": {
      "length": "string",
      "width": "string",
      "height": "string"
    },
    "shipping_required": true,
    "shipping_taxable": true,
    "shipping_class": "string",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "string",
    "rating_count": 0,
    "related_ids": [
      0
    ],
    "upsell_ids": [
      0
    ],
    "cross_sell_ids": [
      0
    ],
    "parent_id": "string",
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
    "variations": [
      0
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
],  'vendor_data': {
  "email": "string",
  "password": "string",
  "store_name": "string",
  "social": [
    "string"
  ],
  "payment": [
    "string"
  ],
  "phone": "string",
  "show_email": "yes",
  "address": [
    "string"
  ],
  "location": "string",
  "banner": "string",
  "icon": "string",
  "gravatar": "string",
  "show_more_tpab": "yes",
  "show_ppp": 0,
  "enable_tnc": "on",
  "store_seo": [
    "string"
  ],
  "dokan_store_time": [
    "string"
  ],
  "enabled": "yes",
  "trusted": "yes"
}
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/dummy-data/import',
  params: {
  'vendor_products' => 'array[object]',
'vendor_data' => 'object'
}, headers: headers

p JSON.parse(result)

```

`POST /dummy-data/import`

> Body parameter

```json
{
  "vendor_products": [
    {
      "id": 0,
      "name": "string",
      "slug": "string",
      "permalink": "http://example.com",
      "date_created": "2019-08-24T14:15:22Z",
      "date_created_gmt": "2019-08-24T14:15:22Z",
      "date_modified": "2019-08-24T14:15:22Z",
      "date_modified_gmt": "2019-08-24T14:15:22Z",
      "type": "simple",
      "status": "draft",
      "featured": true,
      "catalog_visibility": "visible",
      "description": "string",
      "short_description": "string",
      "sku": "string",
      "price": "string",
      "regular_price": "string",
      "sale_price": "string",
      "date_on_sale_from": "2019-08-24T14:15:22Z",
      "date_on_sale_from_gmt": "2019-08-24T14:15:22Z",
      "date_on_sale_to": "2019-08-24T14:15:22Z",
      "date_on_sale_to_gmt": "2019-08-24T14:15:22Z",
      "on_sale": true,
      "purchasable": true,
      "total_sales": "string",
      "virtual": "string",
      "downloadable": "string",
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
      "stock_quantity": "string",
      "in_stock": true,
      "backorders": "no",
      "backorders_allowed": true,
      "backordered": true,
      "sold_individually": "string",
      "weight": "string",
      "dimensions": {
        "length": "string",
        "width": "string",
        "height": "string"
      },
      "shipping_required": true,
      "shipping_taxable": true,
      "shipping_class": "string",
      "shipping_class_id": 0,
      "reviews_allowed": true,
      "average_rating": "string",
      "rating_count": 0,
      "related_ids": [
        0
      ],
      "upsell_ids": [
        0
      ],
      "cross_sell_ids": [
        0
      ],
      "parent_id": "string",
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
      "variations": [
        0
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
  ],
  "vendor_data": {
    "email": "string",
    "password": "string",
    "store_name": "string",
    "social": [
      "string"
    ],
    "payment": [
      "string"
    ],
    "phone": "string",
    "show_email": "yes",
    "address": [
      "string"
    ],
    "location": "string",
    "banner": "string",
    "icon": "string",
    "gravatar": "string",
    "show_more_tpab": "yes",
    "show_ppp": 0,
    "enable_tnc": "on",
    "store_seo": [
      "string"
    ],
    "dokan_store_time": [
      "string"
    ],
    "enabled": "yes",
    "trusted": "yes"
  },
  "vendor_index": 0,
  "total_vendors": 0,
  "result": {
    "imported": [
      0
    ],
    "failed": [
      0
    ],
    "updated": [
      0
    ],
    "skipped": [
      0
    ]
  }
}
```

<h3 id="post__dummy-data_import-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vendor_products|query|array[object]|true|Vendors products data.|
|vendor_data|query|object|true|Vendors profile data.|
|vendor_index|query|number|false|Vendor item index to import.|
|total_vendors|query|integer|false|Total vendors|
|result|query|object|false|none|
|body|body|object|true|none|
|» vendor_products|body|[object]|false|Vendors products data.|
|»» id|body|integer|false|Unique identifier for the resource.|
|»» name|body|string|false|Product name.|
|»» slug|body|string|false|Product slug.|
|»» permalink|body|string(uri)|false|Product URL.|
|»» date_created|body|string(date-time)|false|The date the product was created, in the site's timezone.|
|»» date_created_gmt|body|string(date-time)|false|The date the product was created, as GMT.|
|»» date_modified|body|string(date-time)|false|The date the product was last modified, in the site's timezone.|
|»» date_modified_gmt|body|string(date-time)|false|The date the product was last modified, as GMT.|
|»» type|body|string|true|Product type.|
|»» status|body|string|true|Product status (post status).|
|»» featured|body|boolean|false|Featured product.|
|»» catalog_visibility|body|string|false|Catalog visibility.|
|»» description|body|string|false|Product description.|
|»» short_description|body|string|false|Product short description.|
|»» sku|body|string|false|Unique identifier.|
|»» price|body|string|false|Current product price.|
|»» regular_price|body|string|false|Product regular price.|
|»» sale_price|body|string|false|Product sale price.|
|»» date_on_sale_from|body|string(date-time)|false|Start date of sale price, in the site's timezone.|
|»» date_on_sale_from_gmt|body|string(date-time)|false|Start date of sale price, as GMT.|
|»» date_on_sale_to|body|string(date-time)|false|End date of sale price, in the site's timezone.|
|»» date_on_sale_to_gmt|body|string(date-time)|false|End date of sale price, as GMT.|
|»» on_sale|body|boolean|false|Shows if the product is on sale.|
|»» purchasable|body|boolean|false|Shows if the product can be bought.|
|»» total_sales|body|string|false|Amount of sales.|
|»» virtual|body|string|false|If the product is virtual.|
|»» downloadable|body|string|false|If the product is downloadable.|
|»» downloads|body|[object]|false|List of downloadable files.|
|»»» id|body|string|false|File MD5 hash.|
|»»» name|body|string|false|File name.|
|»»» file|body|string|false|File URL.|
|»» download_limit|body|integer|false|Number of times downloadable files can be downloaded after purchase.|
|»» download_expiry|body|integer|false|Number of days until access to downloadable files expires.|
|»» external_url|body|string(uri)|false|Product external URL. Only for external products.|
|»» button_text|body|string|false|Product external button text. Only for external products.|
|»» tax_status|body|string|false|Tax status.|
|»» tax_class|body|string|false|Tax class.|
|»» manage_stock|body|boolean|false|Stock management at product level.|
|»» stock_quantity|body|string|false|Stock quantity.|
|»» in_stock|body|boolean|false|Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.|
|»» backorders|body|string|false|If managing stock, this controls if backorders are allowed.|
|»» backorders_allowed|body|boolean|false|Shows if backorders are allowed.|
|»» backordered|body|boolean|false|Shows if the product is on backordered.|
|»» sold_individually|body|string|false|Allow one item to be bought in a single order.|
|»» weight|body|string|false|Product weight (kg).|
|»» dimensions|body|object|false|Product dimensions.|
|»»» length|body|string|false|Product length (cm).|
|»»» width|body|string|false|Product width (cm).|
|»»» height|body|string|false|Product height (cm).|
|»» shipping_required|body|boolean|false|Shows if the product need to be shipped.|
|»» shipping_taxable|body|boolean|false|Shows whether or not the product shipping is taxable.|
|»» shipping_class|body|string|false|Shipping class slug.|
|»» shipping_class_id|body|number|false|Shipping class ID.|
|»» reviews_allowed|body|boolean|false|Allow reviews.|
|»» average_rating|body|string|false|Reviews average rating.|
|»» rating_count|body|integer|false|Amount of reviews that the product have.|
|»» related_ids|body|[integer]|false|List of related products IDs.|
|»» upsell_ids|body|[integer]|false|List of up-sell products IDs.|
|»» cross_sell_ids|body|[integer]|false|List of cross-sell products IDs.|
|»» parent_id|body|string|false|Product parent ID.|
|»» purchase_note|body|string|false|Optional note to send the customer after purchase.|
|»» categories|body|[object]|false|List of categories.|
|»»» id|body|integer|false|Category ID.|
|»»» name|body|string|false|Category name.|
|»»» slug|body|string|false|Category slug.|
|»» tags|body|[object]|false|List of tags.|
|»»» id|body|integer|false|Tag ID.|
|»»» name|body|string|false|Tag name.|
|»»» slug|body|string|false|Tag slug.|
|»» images|body|[object]|false|List of images.|
|»»» id|body|integer|false|Image ID.|
|»»» date_created|body|string(date-time)|false|The date the image was created, in the site's timezone.|
|»»» date_created_gmt|body|string(date-time)|false|The date the image was created, as GMT.|
|»»» date_modified|body|string(date-time)|false|The date the image was last modified, in the site's timezone.|
|»»» date_modified_gmt|body|string(date-time)|false|The date the image was last modified, as GMT.|
|»»» src|body|string(uri)|false|Image URL.|
|»»» name|body|string|false|Image name.|
|»»» alt|body|string|false|Image alternative text.|
|»»» position|body|integer|false|Image position. 0 means that the image is featured.|
|»» attributes|body|[object]|false|List of attributes.|
|»»» id|body|integer|false|Attribute ID.|
|»»» name|body|string|false|Attribute name.|
|»»» position|body|integer|false|Attribute position.|
|»»» visible|body|boolean|false|Define if the attribute is visible on the "Additional information" tab in the product's page.|
|»»» variation|body|boolean|false|Define if the attribute can be used as variation.|
|»»» options|body|[string]|false|List of available term names of the attribute.|
|»» default_attributes|body|[object]|false|Defaults variation attributes.|
|»»» id|body|integer|false|Attribute ID.|
|»»» name|body|string|false|Attribute name.|
|»»» option|body|string|false|Selected attribute term name.|
|»» variations|body|[integer]|false|List of variations IDs.|
|»» grouped_products|body|[integer]|false|List of grouped products ID.|
|»» menu_order|body|integer|false|Menu order, used to custom sort products.|
|»» meta_data|body|[object]|false|Meta data.|
|»»» id|body|integer|false|Meta ID.|
|»»» key|body|string|false|Meta key.|
|»»» value|body|string|false|Meta value.|
|» vendor_data|body|object|false|Vendors profile data.|
|»» email|body|string|true|Vendor email.|
|»» password|body|string|false|Vendor password.|
|»» store_name|body|string|true|Vendor store name.|
|»» social|body|[string]|false|Vendor social|
|»» payment|body|[string]|false|Vendor payments|
|»» phone|body|string|true|Vendor phone|
|»» show_email|body|string|false|Vendor show email|
|»» address|body|[string]|false|Vendor address|
|»» location|body|string|false|Vendor location|
|»» banner|body|string|false|Vendor banner|
|»» icon|body|string|false|Vendor icon|
|»» gravatar|body|string|false|Vendor gravatar|
|»» show_more_tpab|body|string|false|Vendor show more tpab|
|»» show_ppp|body|integer|false|Vendor show product per page|
|»» enable_tnc|body|string|false|Enable terms and condition|
|»» store_seo|body|[string]|false|Store seo|
|»» dokan_store_time|body|[string]|false|Store time open close array.|
|»» enabled|body|string|false|Vendor enabled.|
|»» trusted|body|string|false|Vendor is trusted.|
|» vendor_index|body|number|false|Vendor item index to import.|
|» total_vendors|body|integer|false|Total vendors|
|» result|body|object|false|none|
|»» imported|body|[number]|false|none|
|»» failed|body|[number]|false|none|
|»» updated|body|[number]|false|none|
|»» skipped|body|[number]|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|»» type|simple|
|»» type|grouped|
|»» type|external|
|»» type|variable|
|»» status|draft|
|»» status|pending|
|»» status|private|
|»» status|publish|
|»» catalog_visibility|visible|
|»» catalog_visibility|catalog|
|»» catalog_visibility|search|
|»» catalog_visibility|hidden|
|»» tax_status|taxable|
|»» tax_status|shipping|
|»» tax_status|none|
|»» backorders|no|
|»» backorders|notify|
|»» backorders|yes|
|»» show_email|yes|
|»» show_email|no|
|»» show_more_tpab|yes|
|»» show_more_tpab|no|
|»» enable_tnc|on|
|»» enable_tnc|off|
|»» enabled|yes|
|»» enabled|no|
|»» trusted|yes|
|»» trusted|no|

<h3 id="post__dummy-data_import-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__dummy-data_clear

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/dummy-data/clear', array(
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

r = requests.delete('http://dokan-sample.test/dummy-data/clear')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/dummy-data/clear',
  params: {
  }

p JSON.parse(result)

```

`DELETE /dummy-data/clear`

<h3 id="delete__dummy-data_clear-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

