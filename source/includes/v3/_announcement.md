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

## get__announcement

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/announcement', array(
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

r = requests.get('http://dokan-sample.test/announcement')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/announcement',
  params: {
  }

p JSON.parse(result)

```

`GET /announcement`

<h3 id="get__announcement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|vendor_id|query|integer|false|If set, specified vendor announcement will be returned.|
|status|query|string|false|Announcement status, this is a admin only feature|
|read_status|query|string|false|Announcement read status, this is a vendor only feature|
|from|query|string(date-time)|false|Announcement date time from|
|to|query|string(date-time)|false|Announcement date time to|

#### Enumerated Values

|Parameter|Value|
|---|---|
|context|view|
|context|embed|
|context|edit|
|status|all|
|status|publish|
|status|pending|
|status|draft|
|status|future|
|status|trash|
|read_status|read|
|read_status|trash|
|read_status|unread|
|read_status|all|

<h3 id="get__announcement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__announcement

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
    $response = $client->request('POST','http://dokan-sample.test/announcement', array(
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

r = requests.post('http://dokan-sample.test/announcement', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/announcement',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /announcement`

> Body parameter

```json
{
  "notice_id": 0,
  "status": "publish",
  "read_status": "read",
  "announcement_type": "all_seller",
  "announcement_sellers": [
    {
      "id": 0,
      "name": "string",
      "shop_name": "string",
      "email": "string"
    }
  ],
  "sender_ids": [
    0
  ],
  "exclude_seller_ids": [
    0
  ]
}
```

<h3 id="post__announcement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|notice_id|query|integer|false|If returning a single notice, notice id will be available .|
|status|query|string|false|Status of the announcement|
|read_status|query|string|false|Vendor read status of the single notice|
|announcement_type|query|string|false|Send announcement to: this is a admin only field|
|announcement_sellers|query|array[object]|false|Send announcement to: this is a admin only field|
|sender_ids|query|array[integer]|false|Send announcement to: this is a admin only field|
|exclude_seller_ids|query|array[integer]|false|Exclude seller ids|
|body|body|object|true|none|
|» notice_id|body|integer|false|If returning a single notice, notice id will be available .|
|» status|body|string|false|Status of the announcement|
|» read_status|body|string|false|Vendor read status of the single notice|
|» announcement_type|body|string|false|Send announcement to: this is a admin only field|
|» announcement_sellers|body|[object]|false|Send announcement to: this is a admin only field|
|»» id|body|integer|false|Vendor id|
|»» name|body|string|false|Vendor name|
|»» shop_name|body|string|false|Vendor shop name|
|»» email|body|string|false|Vendor email address|
|» sender_ids|body|[integer]|false|Send announcement to: this is a admin only field|
|» exclude_seller_ids|body|[integer]|false|Exclude seller ids|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|publish|
|status|pending|
|status|future|
|status|draft|
|read_status|read|
|read_status|unread|
|read_status|trash|
|announcement_type|all_seller|
|announcement_type|selected_seller|
|announcement_type|enabled_seller|
|announcement_type|disabled_seller|
|announcement_type|featured_seller|
|» status|publish|
|» status|pending|
|» status|future|
|» status|draft|
|» read_status|read|
|» read_status|unread|
|» read_status|trash|
|» announcement_type|all_seller|
|» announcement_type|selected_seller|
|» announcement_type|enabled_seller|
|» announcement_type|disabled_seller|
|» announcement_type|featured_seller|

<h3 id="post__announcement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__announcement_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/announcement/{id}', array(
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

r = requests.get('http://dokan-sample.test/announcement/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/announcement/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /announcement/{id}`

<h3 id="get__announcement_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="get__announcement_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__announcement_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/announcement/{id}', array(
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

r = requests.post('http://dokan-sample.test/announcement/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/announcement/{id}',
  params: {
  }

p JSON.parse(result)

```

`POST /announcement/{id}`

<h3 id="post__announcement_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="post__announcement_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__announcement_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/announcement/{id}', array(
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

r = requests.put('http://dokan-sample.test/announcement/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/announcement/{id}',
  params: {
  }

p JSON.parse(result)

```

`PUT /announcement/{id}`

<h3 id="put__announcement_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="put__announcement_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__announcement_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/announcement/{id}', array(
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

r = requests.patch('http://dokan-sample.test/announcement/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/announcement/{id}',
  params: {
  }

p JSON.parse(result)

```

`PATCH /announcement/{id}`

<h3 id="patch__announcement_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="patch__announcement_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__announcement_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/announcement/{id}', array(
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

r = requests.delete('http://dokan-sample.test/announcement/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/announcement/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /announcement/{id}`

<h3 id="delete__announcement_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|force|query|boolean|false|Force delete announcement.|

<h3 id="delete__announcement_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__announcement_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://dokan-sample.test/announcement/{id}/restore', array(
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

r = requests.post('http://dokan-sample.test/announcement/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.post 'http://dokan-sample.test/announcement/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`POST /announcement/{id}/restore`

<h3 id="post__announcement_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="post__announcement_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__announcement_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','http://dokan-sample.test/announcement/{id}/restore', array(
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

r = requests.put('http://dokan-sample.test/announcement/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.put 'http://dokan-sample.test/announcement/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`PUT /announcement/{id}/restore`

<h3 id="put__announcement_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="put__announcement_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__announcement_{id}_restore

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','http://dokan-sample.test/announcement/{id}/restore', array(
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

r = requests.patch('http://dokan-sample.test/announcement/{id}/restore')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.patch 'http://dokan-sample.test/announcement/{id}/restore',
  params: {
  }

p JSON.parse(result)

```

`PATCH /announcement/{id}/restore`

<h3 id="patch__announcement_{id}_restore-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="patch__announcement_{id}_restore-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__announcement_batch

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
    $response = $client->request('POST','http://dokan-sample.test/announcement/batch', array(
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

r = requests.post('http://dokan-sample.test/announcement/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/announcement/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /announcement/batch`

> Body parameter

```json
{
  "trash": [
    0
  ],
  "delete": [
    0
  ],
  "restore": [
    0
  ]
}
```

<h3 id="post__announcement_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|trash|query|array[integer]|false|Batch trash announcements.|
|delete|query|array[integer]|false|Batch delete announcements.|
|restore|query|array[integer]|false|Batch untrash announcements.|
|body|body|object|true|none|
|» trash|body|[integer]|false|Batch trash announcements.|
|» delete|body|[integer]|false|Batch delete announcements.|
|» restore|body|[integer]|false|Batch untrash announcements.|

<h3 id="post__announcement_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__announcement_batch

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
    $response = $client->request('PUT','http://dokan-sample.test/announcement/batch', array(
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

r = requests.put('http://dokan-sample.test/announcement/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/announcement/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /announcement/batch`

> Body parameter

```json
{
  "trash": [
    0
  ],
  "delete": [
    0
  ],
  "restore": [
    0
  ]
}
```

<h3 id="put__announcement_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|trash|query|array[integer]|false|Batch trash announcements.|
|delete|query|array[integer]|false|Batch delete announcements.|
|restore|query|array[integer]|false|Batch untrash announcements.|
|body|body|object|true|none|
|» trash|body|[integer]|false|Batch trash announcements.|
|» delete|body|[integer]|false|Batch delete announcements.|
|» restore|body|[integer]|false|Batch untrash announcements.|

<h3 id="put__announcement_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__announcement_batch

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
    $response = $client->request('PATCH','http://dokan-sample.test/announcement/batch', array(
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

r = requests.patch('http://dokan-sample.test/announcement/batch', headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/announcement/batch',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /announcement/batch`

> Body parameter

```json
{
  "trash": [
    0
  ],
  "delete": [
    0
  ],
  "restore": [
    0
  ]
}
```

<h3 id="patch__announcement_batch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|trash|query|array[integer]|false|Batch trash announcements.|
|delete|query|array[integer]|false|Batch delete announcements.|
|restore|query|array[integer]|false|Batch untrash announcements.|
|body|body|object|true|none|
|» trash|body|[integer]|false|Batch trash announcements.|
|» delete|body|[integer]|false|Batch delete announcements.|
|» restore|body|[integer]|false|Batch untrash announcements.|

<h3 id="patch__announcement_batch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__announcement_notice_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/announcement/notice/{id}', array(
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

r = requests.get('http://dokan-sample.test/announcement/notice/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/announcement/notice/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /announcement/notice/{id}`

<h3 id="get__announcement_notice_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="get__announcement_notice_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__announcement_notice_{id}

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
    $response = $client->request('POST','http://dokan-sample.test/announcement/notice/{id}', array(
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

r = requests.post('http://dokan-sample.test/announcement/notice/{id}', params={
  'read_status': 'read'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post 'http://dokan-sample.test/announcement/notice/{id}',
  params: {
  'read_status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`POST /announcement/notice/{id}`

> Body parameter

```json
{
  "read_status": "read"
}
```

<h3 id="post__announcement_notice_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|read_status|query|string|true|Announcement read status|
|body|body|object|true|none|
|» read_status|body|string|false|Announcement read status|

#### Enumerated Values

|Parameter|Value|
|---|---|
|read_status|read|
|read_status|unread|
|» read_status|read|
|» read_status|unread|

<h3 id="post__announcement_notice_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## put__announcement_notice_{id}

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
    $response = $client->request('PUT','http://dokan-sample.test/announcement/notice/{id}', array(
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

r = requests.put('http://dokan-sample.test/announcement/notice/{id}', params={
  'read_status': 'read'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'http://dokan-sample.test/announcement/notice/{id}',
  params: {
  'read_status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`PUT /announcement/notice/{id}`

> Body parameter

```json
{
  "read_status": "read"
}
```

<h3 id="put__announcement_notice_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|read_status|query|string|true|Announcement read status|
|body|body|object|true|none|
|» read_status|body|string|false|Announcement read status|

#### Enumerated Values

|Parameter|Value|
|---|---|
|read_status|read|
|read_status|unread|
|» read_status|read|
|» read_status|unread|

<h3 id="put__announcement_notice_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## patch__announcement_notice_{id}

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
    $response = $client->request('PATCH','http://dokan-sample.test/announcement/notice/{id}', array(
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

r = requests.patch('http://dokan-sample.test/announcement/notice/{id}', params={
  'read_status': 'read'
}, headers = headers)

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.patch 'http://dokan-sample.test/announcement/notice/{id}',
  params: {
  'read_status' => 'string'
}, headers: headers

p JSON.parse(result)

```

`PATCH /announcement/notice/{id}`

> Body parameter

```json
{
  "read_status": "read"
}
```

<h3 id="patch__announcement_notice_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|
|read_status|query|string|true|Announcement read status|
|body|body|object|true|none|
|» read_status|body|string|false|Announcement read status|

#### Enumerated Values

|Parameter|Value|
|---|---|
|read_status|read|
|read_status|unread|
|» read_status|read|
|» read_status|unread|

<h3 id="patch__announcement_notice_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete__announcement_notice_{id}

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','http://dokan-sample.test/announcement/notice/{id}', array(
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

r = requests.delete('http://dokan-sample.test/announcement/notice/{id}')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete 'http://dokan-sample.test/announcement/notice/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /announcement/notice/{id}`

<h3 id="delete__announcement_notice_{id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer|true|Unique identifier for the object.|

<h3 id="delete__announcement_notice_{id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__admin_logs

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/admin/logs', array(
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

r = requests.get('http://dokan-sample.test/admin/logs')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/admin/logs',
  params: {
  }

p JSON.parse(result)

```

`GET /admin/logs`

<h3 id="get__admin_logs-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|vendor_id|query|array[string]|false|Vendor IDs to filter form|
|order_id|query|array[string]|false|Order IDs to filter form|
|order_status|query|array[string]|false|Order status to filter form|
|orderby|query|string|false|Filter by column|
|order|query|string|false|Order by type|
|return|query|string|false|How data will be returned|

#### Enumerated Values

|Parameter|Value|
|---|---|
|order|desc|
|order|asc|
|return|all|
|return|ids|
|return|count|

<h3 id="get__admin_logs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

## get__admin_logs_export

> Code samples

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://dokan-sample.test/admin/logs/export', array(
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

r = requests.get('http://dokan-sample.test/admin/logs/export')

print(r.json())

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get 'http://dokan-sample.test/admin/logs/export',
  params: {
  }

p JSON.parse(result)

```

`GET /admin/logs/export`

<h3 id="get__admin_logs_export-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|context|query|string|false|Scope under which the request is made; determines fields present in response.|
|page|query|integer|false|Current page of the collection.|
|per_page|query|integer|false|Maximum number of items to be returned in result set.|
|search|query|string|false|Limit results to those matching a string.|
|vendor_id|query|array[string]|false|Vendor IDs to filter form|
|order_id|query|array[string]|false|Order IDs to filter form|
|order_status|query|array[string]|false|Order status to filter form|
|orderby|query|string|false|Filter by column|
|order|query|string|false|Order by type|
|return|query|string|false|How data will be returned|

#### Enumerated Values

|Parameter|Value|
|---|---|
|order|desc|
|order|asc|
|return|all|
|return|ids|
|return|count|

<h3 id="get__admin_logs_export-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|

<aside class="success">
This operation does not require authentication
</aside>

