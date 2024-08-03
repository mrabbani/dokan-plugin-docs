# STORE-REVIEWS
### ***GET*** 

### HTTP Request 
`***GET*** /store-reviews` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| vendor_id | query | Vendor ID | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /STORE-REVIEWS/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /store-reviews/{id}` 

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
`***POST*** /store-reviews/{id}` 

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
`***PUT*** /store-reviews/{id}` 

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
`***PATCH*** /store-reviews/{id}` 

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
`***DELETE*** /store-reviews/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| force | query | Trash or permanenet delete | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /STORE-REVIEWS/{ID}/RESTORE
### ***POST*** 

### HTTP Request 
`***POST*** /store-reviews/{id}/restore` 

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
`***PUT*** /store-reviews/{id}/restore` 

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
`***PATCH*** /store-reviews/{id}/restore` 

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

## /STORE-REVIEWS/BATCH
### ***POST*** 

### HTTP Request 
`***POST*** /store-reviews/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /store-reviews/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /store-reviews/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ADMIN/SUPPORT-TICKET
### ***GET*** 

### HTTP Request 
`***GET*** /admin/support-ticket` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| filter | query | Finter argumants | No |  |
| orderby | query | Get results order by | No |  |
| order | query | Assendind or decending order | No |  |
| post_status | query | Ticket status | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ADMIN/SUPPORT-TICKET/BATCH
### ***POST*** 

### HTTP Request 
`***POST*** /admin/support-ticket/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /admin/support-ticket/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /admin/support-ticket/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ADMIN/SUPPORT-TICKET/CUSTOMERS
### ***GET*** 

### HTTP Request 
`***GET*** /admin/support-ticket/customers` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ADMIN/SUPPORT-TICKET/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /admin/support-ticket/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier of topic id. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /admin/support-ticket/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier if topic. | Yes |  |
| replay | query | Topic comment or replay | Yes |  |
| vendor_id | query | Store id | Yes |  |
| selected_user | query | Store id | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ADMIN/SUPPORT-TICKET/{ID}/STATUS
### ***POST*** 

### HTTP Request 
`***POST*** /admin/support-ticket/{id}/status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier if topic. | Yes |  |
| status | query | Topic status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ADMIN/SUPPORT-TICKET/{ID}/COMMENT
### ***DELETE*** 

### HTTP Request 
`***DELETE*** /admin/support-ticket/{id}/comment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier of comment. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ADMIN/SUPPORT-TICKET/{ID}/EMAIL-NOTIFICATION
### ***POST*** 

### HTTP Request 
`***POST*** /admin/support-ticket/{id}/email-notification` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier of topic id. | Yes |  |
| notification | query | Enable or disable notification for admin | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
