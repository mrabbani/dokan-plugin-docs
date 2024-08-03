# REQUEST-FOR-QUOTE
## /REQUEST-FOR-QUOTE
### ***GET*** 

### HTTP Request 
`***GET*** /request-for-quote` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| namespace | query |  | No |  |
| context | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /request-for-quote/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /request-for-quote/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/{ID}/RESTORE
### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/{id}/restore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/{id}/restore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/{id}/restore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/BATCH
### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| user_id | query | Unique identifier for the user. | No |  |
| order_id | query | Unique identifier for the order. | No |  |
| quote_title | query | Title of the quote. | No |  |
| status | query | Status of the quote. | No |  |
| customer_info | query | Customer info | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| user_id | query | Unique identifier for the user. | No |  |
| order_id | query | Unique identifier for the order. | No |  |
| quote_title | query | Title of the quote. | No |  |
| status | query | Status of the quote. | No |  |
| customer_info | query | Customer info | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| user_id | query | Unique identifier for the user. | No |  |
| order_id | query | Unique identifier for the order. | No |  |
| quote_title | query | Title of the quote. | No |  |
| status | query | Status of the quote. | No |  |
| customer_info | query | Customer info | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/CONVERT-TO-ORDER
### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/convert-to-order` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| quote_id | query | Request quote id | Yes |  |
| status | query | Request quote status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/QUOTE-RULE
### ***GET*** 

### HTTP Request 
`***GET*** /request-for-quote/quote-rule` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| status | query | Request Quote status | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/quote-rule` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/QUOTE-RULE/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /request-for-quote/quote-rule/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/quote-rule/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/quote-rule/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/quote-rule/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /request-for-quote/quote-rule/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/QUOTE-RULE/BATCH
### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/quote-rule/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/quote-rule/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/quote-rule/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/QUOTE-RULE/{ID}/RESTORE
### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/quote-rule/{id}/restore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/quote-rule/{id}/restore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/quote-rule/{id}/restore` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/CUSTOMERS
### ***GET*** 

### HTTP Request 
`***GET*** /request-for-quote/customers` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| exclude | query | Ensure result set excludes specific IDs. | No |  |
| include | query | Limit result set to specific IDs. | No |  |
| offset | query | Offset the result set by a specific number of items. | No |  |
| order | query | Order sort attribute ascending or descending. | No |  |
| orderby | query | Sort collection by object attribute. | No |  |
| email | query | Limit result set to resources with a specific email. | No |  |
| role | query | Limit result set to resources with a specific role. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/customers` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| email | query | New user email address. | Yes |  |
| first_name | query | Customer first name. | No |  |
| last_name | query | Customer last name. | No |  |
| username | query | New user username. | No |  |
| password | query | New user password. | Yes |  |
| billing | query | List of billing address data. | No |  |
| shipping | query | List of shipping address data. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/CUSTOMERS/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /request-for-quote/customers/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/customers/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| email | query | The email address for the customer. | No |  |
| first_name | query | Customer first name. | No |  |
| last_name | query | Customer last name. | No |  |
| username | query | Customer login name. | No |  |
| password | query | Customer password. | No |  |
| billing | query | List of billing address data. | No |  |
| shipping | query | List of shipping address data. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/customers/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| email | query | The email address for the customer. | No |  |
| first_name | query | Customer first name. | No |  |
| last_name | query | Customer last name. | No |  |
| username | query | Customer login name. | No |  |
| password | query | Customer password. | No |  |
| billing | query | List of billing address data. | No |  |
| shipping | query | List of shipping address data. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/customers/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| email | query | The email address for the customer. | No |  |
| first_name | query | Customer first name. | No |  |
| last_name | query | Customer last name. | No |  |
| username | query | Customer login name. | No |  |
| password | query | Customer password. | No |  |
| billing | query | List of billing address data. | No |  |
| shipping | query | List of shipping address data. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /request-for-quote/customers/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| force | query | Required to be true, as resource does not support trashing. | No |  |
| reassign | query | ID to reassign posts to. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/CUSTOMERS/BATCH
### ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/customers/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| email | query | The email address for the customer. | No |  |
| first_name | query | Customer first name. | No |  |
| last_name | query | Customer last name. | No |  |
| username | query | Customer login name. | No |  |
| password | query | Customer password. | No |  |
| billing | query | List of billing address data. | No |  |
| shipping | query | List of shipping address data. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/customers/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| email | query | The email address for the customer. | No |  |
| first_name | query | Customer first name. | No |  |
| last_name | query | Customer last name. | No |  |
| username | query | Customer login name. | No |  |
| password | query | Customer password. | No |  |
| billing | query | List of billing address data. | No |  |
| shipping | query | List of shipping address data. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/customers/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| email | query | The email address for the customer. | No |  |
| first_name | query | Customer first name. | No |  |
| last_name | query | Customer last name. | No |  |
| username | query | Customer login name. | No |  |
| password | query | Customer password. | No |  |
| billing | query | List of billing address data. | No |  |
| shipping | query | List of shipping address data. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /REQUEST-FOR-QUOTE/ROLES
### ***GET*** 

### HTTP Request 
`***GET*** /request-for-quote/roles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| status | query | Request Quote status | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
