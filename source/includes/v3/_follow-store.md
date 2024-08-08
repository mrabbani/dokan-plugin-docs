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

## get__follow-store

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/follow-store', array(
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

r = requests.get('http://dokan-sample.test/follow-store', params={
  'vendor_id': '0'
})

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/follow-store',
  params: {
  'vendor_id' => 'integer'
}

p JSON.parse(result)

```

`GET /follow-store`

<h3 id="get__follow-store-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|vendor_id|query|integer|true|Vendor id to check if user is following that vendor|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__follow-store-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__follow-store

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
    $response = $client->request('POST','http://dokan-sample.test/follow-store', array(
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

r = requests.post('http://dokan-sample.test/follow-store', params={
  'vendor_id': '0'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/follow-store',
  params: {
  'vendor_id' => 'integer'
}, headers: headers

p JSON.parse(result)

```

`POST /follow-store`

> Body parameter

```json
{
  "context": "view",
  "vendor_id": 0
}
```

<h3 id="post__follow-store-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|vendor_id|query|integer|true|Vendor id to follow or unfollow|
|body|body|object|true|none|
|» context|body|string|false|Scope under which the request is made; determines fields present in response.|
|» vendor_id|body|integer|false|Vendor id to follow or unfollow|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|» context|view|
|» context|edit|

<h3 id="post__follow-store-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__follow-store_followers

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/follow-store/followers', array(
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

r = requests.get('http://dokan-sample.test/follow-store/followers')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/follow-store/followers',
  params: {
  }

p JSON.parse(result)

```

`GET /follow-store/followers`

<h3 id="get__follow-store_followers-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|vendor_id|query|integer|false|Vendor id follow/unfollow|
|search|query|string|false|search followers|
|order|query|string|false|order parameter|
|orderby|query|string|false|order by parameter|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|
|order|asc|
|order|ASC|
|order|desc|
|order|DESC|
|orderby|follower_id|
|orderby|followed_at|

<h3 id="get__follow-store_followers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

