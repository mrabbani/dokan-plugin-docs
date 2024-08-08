# VERIFICATION-METHODS
## /VERIFICATION-METHODS
### ***GET*** 

### HTTP Request 
`***GET*** /verification-methods` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| required | query | The document type is required or not | No |  |
| status | query | The document type is enabled or not | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /verification-methods` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| title | query | Title of the resource. | Yes |  |
| help_text | query | Help Text of the resource. | No |  |
| status | query | The document type status is enabled or not | No |  |
| kind | query | The document type kind | No |  |
| required | query | The document type is required or not | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /VERIFICATION-METHODS/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /verification-methods/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /verification-methods/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| title | query | Title of the resource. | No |  |
| help_text | query | Help Text of the resource. | No |  |
| status | query | The document type status is enabled or not | No |  |
| kind | query | The document type kind | No |  |
| required | query | The document type is required or not | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /verification-methods/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| title | query | Title of the resource. | No |  |
| help_text | query | Help Text of the resource. | No |  |
| status | query | The document type status is enabled or not | No |  |
| kind | query | The document type kind | No |  |
| required | query | The document type is required or not | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /verification-methods/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| title | query | Title of the resource. | No |  |
| help_text | query | Help Text of the resource. | No |  |
| status | query | The document type status is enabled or not | No |  |
| kind | query | The document type kind | No |  |
| required | query | The document type is required or not | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /verification-methods/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| force | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
