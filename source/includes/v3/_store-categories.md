# STORE-CATEGORIES
## /STORE-CATEGORIES
### ***GET*** 

### HTTP Request 
`***GET*** /store-categories` 

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
| orderby | query | Sort collection by term attribute. | No |  |
| hide_empty | query | Whether to hide terms not assigned to any posts. | No |  |
| post | query | Limit result set to terms assigned to a specific post. | No |  |
| slug | query | Limit result set to terms with one or more specific slugs. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /store-categories` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| description | query | HTML description of the term. | No |  |
| name | query | HTML title for the term. | Yes |  |
| slug | query | An alphanumeric identifier for the term unique to its type. | No |  |
| meta | query | Meta fields. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /STORE-CATEGORIES/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /store-categories/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the term. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /store-categories/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the term. | Yes |  |
| description | query | HTML description of the term. | No |  |
| name | query | HTML title for the term. | No |  |
| slug | query | An alphanumeric identifier for the term unique to its type. | No |  |
| meta | query | Meta fields. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /store-categories/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the term. | Yes |  |
| description | query | HTML description of the term. | No |  |
| name | query | HTML title for the term. | No |  |
| slug | query | An alphanumeric identifier for the term unique to its type. | No |  |
| meta | query | Meta fields. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /store-categories/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the term. | Yes |  |
| description | query | HTML description of the term. | No |  |
| name | query | HTML title for the term. | No |  |
| slug | query | An alphanumeric identifier for the term unique to its type. | No |  |
| meta | query | Meta fields. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /store-categories/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the term. | Yes |  |
| force | query | Required to be true, as terms do not support trashing. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /STORE-CATEGORIES/DEFAULT-CATEGORY
### ***GET*** 

### HTTP Request 
`***GET*** /store-categories/default-category` 

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
| orderby | query | Sort collection by term attribute. | No |  |
| hide_empty | query | Whether to hide terms not assigned to any posts. | No |  |
| post | query | Limit result set to terms assigned to a specific post. | No |  |
| slug | query | Limit result set to terms with one or more specific slugs. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /store-categories/default-category` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| description | query | HTML description of the term. | No |  |
| name | query | HTML title for the term. | No |  |
| slug | query | An alphanumeric identifier for the term unique to its type. | No |  |
| meta | query | Meta fields. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /store-categories/default-category` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| description | query | HTML description of the term. | No |  |
| name | query | HTML title for the term. | No |  |
| slug | query | An alphanumeric identifier for the term unique to its type. | No |  |
| meta | query | Meta fields. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /store-categories/default-category` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| description | query | HTML description of the term. | No |  |
| name | query | HTML title for the term. | No |  |
| slug | query | An alphanumeric identifier for the term unique to its type. | No |  |
| meta | query | Meta fields. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
