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

## get__request-for-quote

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/request-for-quote', array(
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

r = requests.get('http://dokan-sample.test/request-for-quote')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/request-for-quote',
  params: {
  }

p JSON.parse(result)

```

`GET /request-for-quote`

<h3 id="get__request-for-quote-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|namespace|query|string|false|none|
|context|query|string|false|none|

<h3 id="get__request-for-quote-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/request-for-quote',
  params: {
  }

p JSON.parse(result)

```

`POST /request-for-quote`

<h3 id="post__request-for-quote-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__request-for-quote_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/request-for-quote/{id}', array(
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

r = requests.get('http://dokan-sample.test/request-for-quote/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/request-for-quote/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /request-for-quote/{id}`

<h3 id="get__request-for-quote_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="get__request-for-quote_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/{id}', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/request-for-quote/{id}',
  params: {
  }

p JSON.parse(result)

```

`POST /request-for-quote/{id}`

<h3 id="post__request-for-quote_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="post__request-for-quote_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/{id}', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/request-for-quote/{id}',
  params: {
  }

p JSON.parse(result)

```

`PUT /request-for-quote/{id}`

<h3 id="put__request-for-quote_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="put__request-for-quote_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/{id}', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/{id}',
  params: {
  }

p JSON.parse(result)

```

`PATCH /request-for-quote/{id}`

<h3 id="patch__request-for-quote_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="patch__request-for-quote_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__request-for-quote_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/request-for-quote/{id}', array(
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

r = requests.delete('http://dokan-sample.test/request-for-quote/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/request-for-quote/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /request-for-quote/{id}`

<h3 id="delete__request-for-quote_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="delete__request-for-quote_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/{id}/restore', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/request-for-quote/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`POST /request-for-quote/{id}/restore`

<h3 id="post__request-for-quote_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="post__request-for-quote_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/{id}/restore', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/request-for-quote/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`PUT /request-for-quote/{id}/restore`

<h3 id="put__request-for-quote_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="put__request-for-quote_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/{id}/restore', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`PATCH /request-for-quote/{id}/restore`

<h3 id="patch__request-for-quote_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="patch__request-for-quote_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_batch

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
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/batch', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/request-for-quote/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /request-for-quote/batch`

> Body parameter

```json
{
  "user_id": 0,
  "order_id": 0,
  "quote_title": "string",
  "status": "string",
  "customer_info": "string"
}
```

<h3 id="post__request-for-quote_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|user_id|query|integer|false|Unique identifier for the user.|
|order_id|query|integer|false|Unique identifier for the order.|
|quote_title|query|string|false|Title of the quote.|
|status|query|string|false|Status of the quote.|
|customer_info|query|string|false|Customer info|
|body|body|object|true|none|
|» user_id|body|integer|false|Unique identifier for the user.|
|» order_id|body|integer|false|Unique identifier for the order.|
|» quote_title|body|string|false|Title of the quote.|
|» status|body|string|false|Status of the quote.|
|» customer_info|body|string|false|Customer info|

<h3 id="post__request-for-quote_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/batch', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/request-for-quote/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /request-for-quote/batch`

> Body parameter

```json
{
  "user_id": 0,
  "order_id": 0,
  "quote_title": "string",
  "status": "string",
  "customer_info": "string"
}
```

<h3 id="put__request-for-quote_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|user_id|query|integer|false|Unique identifier for the user.|
|order_id|query|integer|false|Unique identifier for the order.|
|quote_title|query|string|false|Title of the quote.|
|status|query|string|false|Status of the quote.|
|customer_info|query|string|false|Customer info|
|body|body|object|true|none|
|» user_id|body|integer|false|Unique identifier for the user.|
|» order_id|body|integer|false|Unique identifier for the order.|
|» quote_title|body|string|false|Title of the quote.|
|» status|body|string|false|Status of the quote.|
|» customer_info|body|string|false|Customer info|

<h3 id="put__request-for-quote_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/batch', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /request-for-quote/batch`

> Body parameter

```json
{
  "user_id": 0,
  "order_id": 0,
  "quote_title": "string",
  "status": "string",
  "customer_info": "string"
}
```

<h3 id="patch__request-for-quote_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|user_id|query|integer|false|Unique identifier for the user.|
|order_id|query|integer|false|Unique identifier for the order.|
|quote_title|query|string|false|Title of the quote.|
|status|query|string|false|Status of the quote.|
|customer_info|query|string|false|Customer info|
|body|body|object|true|none|
|» user_id|body|integer|false|Unique identifier for the user.|
|» order_id|body|integer|false|Unique identifier for the order.|
|» quote_title|body|string|false|Title of the quote.|
|» status|body|string|false|Status of the quote.|
|» customer_info|body|string|false|Customer info|

<h3 id="patch__request-for-quote_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_convert-to-order

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
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/convert-to-order', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/convert-to-order', params={
  'quote_id': '0',  'status': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/request-for-quote/convert-to-order',
  params: {
  'quote_id' => 'number',
'status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /request-for-quote/convert-to-order`

> Body parameter

```json
{
  "quote_id": 0,
  "status": "string"
}
```

<h3 id="post__request-for-quote_convert-to-order-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|quote_id|query|number|true|Request quote id|
|status|query|string|true|Request quote status|
|body|body|object|true|none|
|» quote_id|body|number|false|Request quote id|
|» status|body|string|false|Request quote status|

<h3 id="post__request-for-quote_convert-to-order-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__request-for-quote_quote-rule

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/request-for-quote/quote-rule', array(
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

r = requests.get('http://dokan-sample.test/request-for-quote/quote-rule')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/request-for-quote/quote-rule',
  params: {
  }

p JSON.parse(result)

```

`GET /request-for-quote/quote-rule`

<h3 id="get__request-for-quote_quote-rule-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|status|query|string|false|Request Quote status|

<h3 id="get__request-for-quote_quote-rule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_quote-rule

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/quote-rule', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/quote-rule')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/request-for-quote/quote-rule',
  params: {
  }

p JSON.parse(result)

```

`POST /request-for-quote/quote-rule`

<h3 id="post__request-for-quote_quote-rule-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__request-for-quote_quote-rule_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/request-for-quote/quote-rule/{id}', array(
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

r = requests.get('http://dokan-sample.test/request-for-quote/quote-rule/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/request-for-quote/quote-rule/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /request-for-quote/quote-rule/{id}`

<h3 id="get__request-for-quote_quote-rule_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="get__request-for-quote_quote-rule_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_quote-rule_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/quote-rule/{id}', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/quote-rule/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/request-for-quote/quote-rule/{id}',
  params: {
  }

p JSON.parse(result)

```

`POST /request-for-quote/quote-rule/{id}`

<h3 id="post__request-for-quote_quote-rule_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="post__request-for-quote_quote-rule_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_quote-rule_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/quote-rule/{id}', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/quote-rule/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/request-for-quote/quote-rule/{id}',
  params: {
  }

p JSON.parse(result)

```

`PUT /request-for-quote/quote-rule/{id}`

<h3 id="put__request-for-quote_quote-rule_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="put__request-for-quote_quote-rule_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_quote-rule_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/quote-rule/{id}', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/quote-rule/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/quote-rule/{id}',
  params: {
  }

p JSON.parse(result)

```

`PATCH /request-for-quote/quote-rule/{id}`

<h3 id="patch__request-for-quote_quote-rule_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="patch__request-for-quote_quote-rule_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__request-for-quote_quote-rule_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/request-for-quote/quote-rule/{id}', array(
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

r = requests.delete('http://dokan-sample.test/request-for-quote/quote-rule/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/request-for-quote/quote-rule/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /request-for-quote/quote-rule/{id}`

<h3 id="delete__request-for-quote_quote-rule_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="delete__request-for-quote_quote-rule_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_quote-rule_batch

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/quote-rule/batch', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/quote-rule/batch')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/request-for-quote/quote-rule/batch',
  params: {
  }

p JSON.parse(result)

```

`POST /request-for-quote/quote-rule/batch`

<h3 id="post__request-for-quote_quote-rule_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_quote-rule_batch

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/quote-rule/batch', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/quote-rule/batch')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/request-for-quote/quote-rule/batch',
  params: {
  }

p JSON.parse(result)

```

`PUT /request-for-quote/quote-rule/batch`

<h3 id="put__request-for-quote_quote-rule_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_quote-rule_batch

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/quote-rule/batch', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/quote-rule/batch')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/quote-rule/batch',
  params: {
  }

p JSON.parse(result)

```

`PATCH /request-for-quote/quote-rule/batch`

<h3 id="patch__request-for-quote_quote-rule_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_quote-rule_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`POST /request-for-quote/quote-rule/{id}/restore`

<h3 id="post__request-for-quote_quote-rule_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="post__request-for-quote_quote-rule_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_quote-rule_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`PUT /request-for-quote/quote-rule/{id}/restore`

<h3 id="put__request-for-quote_quote-rule_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="put__request-for-quote_quote-rule_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_quote-rule_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/quote-rule/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`PATCH /request-for-quote/quote-rule/{id}/restore`

<h3 id="patch__request-for-quote_quote-rule_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="patch__request-for-quote_quote-rule_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__request-for-quote_customers

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/request-for-quote/customers', array(
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

r = requests.get('http://dokan-sample.test/request-for-quote/customers')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/request-for-quote/customers',
  params: {
  }

p JSON.parse(result)

```

`GET /request-for-quote/customers`

<h3 id="get__request-for-quote_customers-parameters">Parameters</h3>

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
|orderby|query|string|false|Sort collection by object attribute.|
|email|query|string(email)|false|Limit result set to resources with a specific email.|
|role|query|string|false|Limit result set to resources with a specific role.|

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
|orderby|registered_date|
|role|all|
|role|administrator|
|role|editor|
|role|author|
|role|contributor|
|role|subscriber|
|role|seller|
|role|customer|
|role|shop_manager|
|role|vendor_staff|
|role|cashier|
|role|translator|
|role|erp_hr_manager|
|role|employee|
|role|erp_ac_manager|

<h3 id="get__request-for-quote_customers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_customers

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
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/customers', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/customers', params={
  'email': 'string',  'password': 'string'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/request-for-quote/customers',
  params: {
  'email' => 'string',
'password' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /request-for-quote/customers`

> Body parameter

```json
{
  "email": "string",
  "first_name": "string",
  "last_name": "string",
  "username": "string",
  "password": "string",
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
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": [
        "string"
      ]
    }
  ]
}
```

<h3 id="post__request-for-quote_customers-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|email|query|string|true|New user email address.|
|first_name|query|string|false|Customer first name.|
|last_name|query|string|false|Customer last name.|
|username|query|string|false|New user username.|
|password|query|string|true|New user password.|
|billing|query|object|false|List of billing address data.|
|shipping|query|object|false|List of shipping address data.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» email|body|string|false|New user email address.|
|» first_name|body|string|false|Customer first name.|
|» last_name|body|string|false|Customer last name.|
|» username|body|string|false|New user username.|
|» password|body|string|false|New user password.|
|» billing|body|object|false|List of billing address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|List of shipping address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|[string]|false|Meta value.|

<h3 id="post__request-for-quote_customers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__request-for-quote_customers_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/request-for-quote/customers/{id}', array(
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

r = requests.get('http://dokan-sample.test/request-for-quote/customers/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/request-for-quote/customers/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /request-for-quote/customers/{id}`

<h3 id="get__request-for-quote_customers_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|edit|

<h3 id="get__request-for-quote_customers_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_customers_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/customers/{id}', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/customers/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/request-for-quote/customers/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /request-for-quote/customers/{id}`

> Body parameter

```json
{
  "email": "user@example.com",
  "first_name": "string",
  "last_name": "string",
  "username": "string",
  "password": "string",
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
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": [
        "string"
      ]
    }
  ]
}
```

<h3 id="post__request-for-quote_customers_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|email|query|string(email)|false|The email address for the customer.|
|first_name|query|string|false|Customer first name.|
|last_name|query|string|false|Customer last name.|
|username|query|string|false|Customer login name.|
|password|query|string|false|Customer password.|
|billing|query|object|false|List of billing address data.|
|shipping|query|object|false|List of shipping address data.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» email|body|string(email)|false|The email address for the customer.|
|» first_name|body|string|false|Customer first name.|
|» last_name|body|string|false|Customer last name.|
|» username|body|string|false|Customer login name.|
|» password|body|string|false|Customer password.|
|» billing|body|object|false|List of billing address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|List of shipping address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|[string]|false|Meta value.|

<h3 id="post__request-for-quote_customers_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_customers_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/customers/{id}', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/customers/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/request-for-quote/customers/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /request-for-quote/customers/{id}`

> Body parameter

```json
{
  "email": "user@example.com",
  "first_name": "string",
  "last_name": "string",
  "username": "string",
  "password": "string",
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
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": [
        "string"
      ]
    }
  ]
}
```

<h3 id="put__request-for-quote_customers_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|email|query|string(email)|false|The email address for the customer.|
|first_name|query|string|false|Customer first name.|
|last_name|query|string|false|Customer last name.|
|username|query|string|false|Customer login name.|
|password|query|string|false|Customer password.|
|billing|query|object|false|List of billing address data.|
|shipping|query|object|false|List of shipping address data.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» email|body|string(email)|false|The email address for the customer.|
|» first_name|body|string|false|Customer first name.|
|» last_name|body|string|false|Customer last name.|
|» username|body|string|false|Customer login name.|
|» password|body|string|false|Customer password.|
|» billing|body|object|false|List of billing address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|List of shipping address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|[string]|false|Meta value.|

<h3 id="put__request-for-quote_customers_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_customers_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/customers/{id}', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/customers/{id}', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/customers/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /request-for-quote/customers/{id}`

> Body parameter

```json
{
  "email": "user@example.com",
  "first_name": "string",
  "last_name": "string",
  "username": "string",
  "password": "string",
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
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": [
        "string"
      ]
    }
  ]
}
```

<h3 id="patch__request-for-quote_customers_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|email|query|string(email)|false|The email address for the customer.|
|first_name|query|string|false|Customer first name.|
|last_name|query|string|false|Customer last name.|
|username|query|string|false|Customer login name.|
|password|query|string|false|Customer password.|
|billing|query|object|false|List of billing address data.|
|shipping|query|object|false|List of shipping address data.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» email|body|string(email)|false|The email address for the customer.|
|» first_name|body|string|false|Customer first name.|
|» last_name|body|string|false|Customer last name.|
|» username|body|string|false|Customer login name.|
|» password|body|string|false|Customer password.|
|» billing|body|object|false|List of billing address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|List of shipping address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|[string]|false|Meta value.|

<h3 id="patch__request-for-quote_customers_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__request-for-quote_customers_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/request-for-quote/customers/{id}', array(
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

r = requests.delete('http://dokan-sample.test/request-for-quote/customers/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/request-for-quote/customers/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /request-for-quote/customers/{id}`

<h3 id="delete__request-for-quote_customers_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the resource.|
|force|query|boolean|false|Required to be true, as resource does not support trashing.|
|reassign|query|integer|false|ID to reassign posts to.|

<h3 id="delete__request-for-quote_customers_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__request-for-quote_customers_batch

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
    $response = $client->request('POST','http://dokan-sample.test/request-for-quote/customers/batch', array(
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

r = requests.post('http://dokan-sample.test/request-for-quote/customers/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/request-for-quote/customers/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /request-for-quote/customers/batch`

> Body parameter

```json
{
  "email": "user@example.com",
  "first_name": "string",
  "last_name": "string",
  "username": "string",
  "password": "string",
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
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": [
        "string"
      ]
    }
  ]
}
```

<h3 id="post__request-for-quote_customers_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|email|query|string(email)|false|The email address for the customer.|
|first_name|query|string|false|Customer first name.|
|last_name|query|string|false|Customer last name.|
|username|query|string|false|Customer login name.|
|password|query|string|false|Customer password.|
|billing|query|object|false|List of billing address data.|
|shipping|query|object|false|List of shipping address data.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» email|body|string(email)|false|The email address for the customer.|
|» first_name|body|string|false|Customer first name.|
|» last_name|body|string|false|Customer last name.|
|» username|body|string|false|Customer login name.|
|» password|body|string|false|Customer password.|
|» billing|body|object|false|List of billing address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|List of shipping address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|[string]|false|Meta value.|

<h3 id="post__request-for-quote_customers_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__request-for-quote_customers_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/request-for-quote/customers/batch', array(
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

r = requests.put('http://dokan-sample.test/request-for-quote/customers/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/request-for-quote/customers/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /request-for-quote/customers/batch`

> Body parameter

```json
{
  "email": "user@example.com",
  "first_name": "string",
  "last_name": "string",
  "username": "string",
  "password": "string",
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
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": [
        "string"
      ]
    }
  ]
}
```

<h3 id="put__request-for-quote_customers_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|email|query|string(email)|false|The email address for the customer.|
|first_name|query|string|false|Customer first name.|
|last_name|query|string|false|Customer last name.|
|username|query|string|false|Customer login name.|
|password|query|string|false|Customer password.|
|billing|query|object|false|List of billing address data.|
|shipping|query|object|false|List of shipping address data.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» email|body|string(email)|false|The email address for the customer.|
|» first_name|body|string|false|Customer first name.|
|» last_name|body|string|false|Customer last name.|
|» username|body|string|false|Customer login name.|
|» password|body|string|false|Customer password.|
|» billing|body|object|false|List of billing address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|List of shipping address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|[string]|false|Meta value.|

<h3 id="put__request-for-quote_customers_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__request-for-quote_customers_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/request-for-quote/customers/batch', array(
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

r = requests.patch('http://dokan-sample.test/request-for-quote/customers/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/request-for-quote/customers/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /request-for-quote/customers/batch`

> Body parameter

```json
{
  "email": "user@example.com",
  "first_name": "string",
  "last_name": "string",
  "username": "string",
  "password": "string",
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
  "meta_data": [
    {
      "id": 0,
      "key": "string",
      "value": [
        "string"
      ]
    }
  ]
}
```

<h3 id="patch__request-for-quote_customers_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|email|query|string(email)|false|The email address for the customer.|
|first_name|query|string|false|Customer first name.|
|last_name|query|string|false|Customer last name.|
|username|query|string|false|Customer login name.|
|password|query|string|false|Customer password.|
|billing|query|object|false|List of billing address data.|
|shipping|query|object|false|List of shipping address data.|
|meta_data|query|array[object]|false|Meta data.|
|body|body|object|true|none|
|» email|body|string(email)|false|The email address for the customer.|
|» first_name|body|string|false|Customer first name.|
|» last_name|body|string|false|Customer last name.|
|» username|body|string|false|Customer login name.|
|» password|body|string|false|Customer password.|
|» billing|body|object|false|List of billing address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|»» email|body|string(email)|false|Email address.|
|»» phone|body|string|false|Phone number.|
|» shipping|body|object|false|List of shipping address data.|
|»» first_name|body|string|false|First name.|
|»» last_name|body|string|false|Last name.|
|»» company|body|string|false|Company name.|
|»» address_1|body|string|false|Address line 1|
|»» address_2|body|string|false|Address line 2|
|»» city|body|string|false|City name.|
|»» state|body|string|false|ISO code or name of the state, province or district.|
|»» postcode|body|string|false|Postal code.|
|»» country|body|string|false|ISO code of the country.|
|» meta_data|body|[object]|false|Meta data.|
|»» id|body|integer|false|Meta ID.|
|»» key|body|string|false|Meta key.|
|»» value|body|[string]|false|Meta value.|

<h3 id="patch__request-for-quote_customers_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__request-for-quote_roles

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/request-for-quote/roles', array(
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

r = requests.get('http://dokan-sample.test/request-for-quote/roles')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/request-for-quote/roles',
  params: {
  }

p JSON.parse(result)

```

`GET /request-for-quote/roles`

<h3 id="get__request-for-quote_roles-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|status|query|string|false|Request Quote status|

<h3 id="get__request-for-quote_roles-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

