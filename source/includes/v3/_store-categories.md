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

## get__store-categories

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/store-categories', array(
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

r = requests.get('http://dokan-sample.test/store-categories')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/store-categories',
  params: {
  }

p JSON.parse(result)

```

`GET /store-categories`

<h3 id="get__store-categories-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|exclude|query|array[integer]|false|Ensure result set excludes specific IDs.|
|include|query|array[integer]|false|Limit result set to specific IDs.|
|offset|query|integer|false|Offset the result set by a specific number of items.|
|order|query|string|false|Order sort attribute ascending or descending.|
|orderby|query|string|false|Sort collection by term attribute.|
|hide_empty|query|boolean|false|Whether to hide terms not assigned to any posts.|
|post|query|integer|false|Limit result set to terms assigned to a specific post.|
|slug|query|array[string]|false|Limit result set to terms with one or more specific slugs.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|embed|
|context|edit|
|order|asc|
|order|desc|
|orderby|id|
|orderby|include|
|orderby|name|
|orderby|slug|
|orderby|include_slugs|
|orderby|term_group|
|orderby|description|
|orderby|count|

<h3 id="get__store-categories-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__store-categories

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
    $response = $client->request('POST','http://dokan-sample.test/store-categories', array(
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

r = requests.post('http://dokan-sample.test/store-categories', params={
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

result = RestClient.post 'http://dokan-sample.test/store-categories',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /store-categories`

> Body parameter

```json
{
  "description": "string",
  "name": "string",
  "slug": "string",
  "meta": {}
}
```

<h3 id="post__store-categories-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|description|query|string|false|HTML description of the term.|
|name|query|string|true|HTML title for the term.|
|slug|query|string|false|An alphanumeric identifier for the term unique to its type.|
|meta|query|object|false|Meta fields.|
|body|body|object|true|none|
|» description|body|string|false|HTML description of the term.|
|» name|body|string|false|HTML title for the term.|
|» slug|body|string|false|An alphanumeric identifier for the term unique to its type.|
|» meta|body|object|false|Meta fields.|

<h3 id="post__store-categories-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__store-categories_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/store-categories/{id}', array(
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

r = requests.get('http://dokan-sample.test/store-categories/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/store-categories/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /store-categories/{id}`

<h3 id="get__store-categories_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the term.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|embed|
|context|edit|

<h3 id="get__store-categories_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__store-categories_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/store-categories/{id}', array(
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

r = requests.post('http://dokan-sample.test/store-categories/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/store-categories/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /store-categories/{id}`

> Body parameter

```json
{
  "description": "string",
  "name": "string",
  "slug": "string",
  "meta": {}
}
```

<h3 id="post__store-categories_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the term.|
|description|query|string|false|HTML description of the term.|
|name|query|string|false|HTML title for the term.|
|slug|query|string|false|An alphanumeric identifier for the term unique to its type.|
|meta|query|object|false|Meta fields.|
|body|body|object|true|none|
|» description|body|string|false|HTML description of the term.|
|» name|body|string|false|HTML title for the term.|
|» slug|body|string|false|An alphanumeric identifier for the term unique to its type.|
|» meta|body|object|false|Meta fields.|

<h3 id="post__store-categories_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__store-categories_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/store-categories/{id}', array(
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

r = requests.put('http://dokan-sample.test/store-categories/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/store-categories/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /store-categories/{id}`

> Body parameter

```json
{
  "description": "string",
  "name": "string",
  "slug": "string",
  "meta": {}
}
```

<h3 id="put__store-categories_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the term.|
|description|query|string|false|HTML description of the term.|
|name|query|string|false|HTML title for the term.|
|slug|query|string|false|An alphanumeric identifier for the term unique to its type.|
|meta|query|object|false|Meta fields.|
|body|body|object|true|none|
|» description|body|string|false|HTML description of the term.|
|» name|body|string|false|HTML title for the term.|
|» slug|body|string|false|An alphanumeric identifier for the term unique to its type.|
|» meta|body|object|false|Meta fields.|

<h3 id="put__store-categories_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__store-categories_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/store-categories/{id}', array(
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

r = requests.patch('http://dokan-sample.test/store-categories/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/store-categories/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /store-categories/{id}`

> Body parameter

```json
{
  "description": "string",
  "name": "string",
  "slug": "string",
  "meta": {}
}
```

<h3 id="patch__store-categories_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the term.|
|description|query|string|false|HTML description of the term.|
|name|query|string|false|HTML title for the term.|
|slug|query|string|false|An alphanumeric identifier for the term unique to its type.|
|meta|query|object|false|Meta fields.|
|body|body|object|true|none|
|» description|body|string|false|HTML description of the term.|
|» name|body|string|false|HTML title for the term.|
|» slug|body|string|false|An alphanumeric identifier for the term unique to its type.|
|» meta|body|object|false|Meta fields.|

<h3 id="patch__store-categories_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__store-categories_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/store-categories/{id}', array(
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

r = requests.delete('http://dokan-sample.test/store-categories/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/store-categories/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /store-categories/{id}`

<h3 id="delete__store-categories_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the term.|
|force|query|boolean|false|Required to be true, as terms do not support trashing.|

<h3 id="delete__store-categories_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__store-categories_default-category

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/store-categories/default-category', array(
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

r = requests.get('http://dokan-sample.test/store-categories/default-category')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/store-categories/default-category',
  params: {
  }

p JSON.parse(result)

```

`GET /store-categories/default-category`

<h3 id="get__store-categories_default-category-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|exclude|query|array[integer]|false|Ensure result set excludes specific IDs.|
|include|query|array[integer]|false|Limit result set to specific IDs.|
|offset|query|integer|false|Offset the result set by a specific number of items.|
|order|query|string|false|Order sort attribute ascending or descending.|
|orderby|query|string|false|Sort collection by term attribute.|
|hide_empty|query|boolean|false|Whether to hide terms not assigned to any posts.|
|post|query|integer|false|Limit result set to terms assigned to a specific post.|
|slug|query|array[string]|false|Limit result set to terms with one or more specific slugs.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|embed|
|context|edit|
|order|asc|
|order|desc|
|orderby|id|
|orderby|include|
|orderby|name|
|orderby|slug|
|orderby|include_slugs|
|orderby|term_group|
|orderby|description|
|orderby|count|

<h3 id="get__store-categories_default-category-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__store-categories_default-category

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
    $response = $client->request('POST','http://dokan-sample.test/store-categories/default-category', array(
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

r = requests.post('http://dokan-sample.test/store-categories/default-category', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/store-categories/default-category',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /store-categories/default-category`

> Body parameter

```json
{
  "description": "string",
  "name": "string",
  "slug": "string",
  "meta": {}
}
```

<h3 id="post__store-categories_default-category-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|description|query|string|false|HTML description of the term.|
|name|query|string|false|HTML title for the term.|
|slug|query|string|false|An alphanumeric identifier for the term unique to its type.|
|meta|query|object|false|Meta fields.|
|body|body|object|true|none|
|» description|body|string|false|HTML description of the term.|
|» name|body|string|false|HTML title for the term.|
|» slug|body|string|false|An alphanumeric identifier for the term unique to its type.|
|» meta|body|object|false|Meta fields.|

<h3 id="post__store-categories_default-category-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__store-categories_default-category

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
    $response = $client->request('PUT','http://dokan-sample.test/store-categories/default-category', array(
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

r = requests.put('http://dokan-sample.test/store-categories/default-category', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/store-categories/default-category',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /store-categories/default-category`

> Body parameter

```json
{
  "description": "string",
  "name": "string",
  "slug": "string",
  "meta": {}
}
```

<h3 id="put__store-categories_default-category-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|description|query|string|false|HTML description of the term.|
|name|query|string|false|HTML title for the term.|
|slug|query|string|false|An alphanumeric identifier for the term unique to its type.|
|meta|query|object|false|Meta fields.|
|body|body|object|true|none|
|» description|body|string|false|HTML description of the term.|
|» name|body|string|false|HTML title for the term.|
|» slug|body|string|false|An alphanumeric identifier for the term unique to its type.|
|» meta|body|object|false|Meta fields.|

<h3 id="put__store-categories_default-category-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__store-categories_default-category

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
    $response = $client->request('PATCH','http://dokan-sample.test/store-categories/default-category', array(
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

r = requests.patch('http://dokan-sample.test/store-categories/default-category', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/store-categories/default-category',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /store-categories/default-category`

> Body parameter

```json
{
  "description": "string",
  "name": "string",
  "slug": "string",
  "meta": {}
}
```

<h3 id="patch__store-categories_default-category-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|description|query|string|false|HTML description of the term.|
|name|query|string|false|HTML title for the term.|
|slug|query|string|false|An alphanumeric identifier for the term unique to its type.|
|meta|query|object|false|Meta fields.|
|body|body|object|true|none|
|» description|body|string|false|HTML description of the term.|
|» name|body|string|false|HTML title for the term.|
|» slug|body|string|false|An alphanumeric identifier for the term unique to its type.|
|» meta|body|object|false|Meta fields.|

<h3 id="patch__store-categories_default-category-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

