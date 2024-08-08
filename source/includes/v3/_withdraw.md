# WITHDRAW
## /WITHDRAW
### ***GET*** 

### HTTP Request 
`***GET*** /withdraw` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| ids | query | IDs of withdraws | No |  |
| is_export | query | Is withdraws exportable | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /withdraw` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| user_id | query | Requested User ID | No |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | Yes |  |
| status | query | Withdraw status | No |  |
| method | query | Withdraw Method | Yes |  |
| note | query | Withdraw Notes | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /WITHDRAW/BALANCE
### ***GET*** 

### HTTP Request 
`***GET*** /withdraw/balance` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /WITHDRAW/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /withdraw/{id}` 

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
`***POST*** /withdraw/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| user_id | query | Requested User ID | No |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | No |  |
| status | query | Withdraw status | No |  |
| method | query | Withdraw Method | No |  |
| note | query | Withdraw Notes | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /withdraw/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| user_id | query | Requested User ID | No |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | No |  |
| status | query | Withdraw status | No |  |
| method | query | Withdraw Method | No |  |
| note | query | Withdraw Notes | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /withdraw/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| user_id | query | Requested User ID | No |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | No |  |
| status | query | Withdraw status | No |  |
| method | query | Withdraw Method | No |  |
| note | query | Withdraw Notes | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /withdraw/{id}` 

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

## /WITHDRAW/PAYMENT_METHODS
### ***GET*** 

### HTTP Request 
`***GET*** /withdraw/payment_methods` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /WITHDRAW/BATCH
### ***POST*** 

### HTTP Request 
`***POST*** /withdraw/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| approved | query | List of withdraw IDs to be approved | No |  |
| cancelled | query | List of withdraw IDs to be cancelled | No |  |
| delete | query | List of withdraw IDs to be deleted | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /withdraw/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| approved | query | List of withdraw IDs to be approved | No |  |
| cancelled | query | List of withdraw IDs to be cancelled | No |  |
| delete | query | List of withdraw IDs to be deleted | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /withdraw/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| approved | query | List of withdraw IDs to be approved | No |  |
| cancelled | query | List of withdraw IDs to be cancelled | No |  |
| delete | query | List of withdraw IDs to be deleted | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /WITHDRAW/CHARGES
### ***GET*** 

### HTTP Request 
`***GET*** /withdraw/charges` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /WITHDRAW/CHARGE
### ***GET*** 

### HTTP Request 
`***GET*** /withdraw/charge` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| method | query | Withdraw method key | Yes |  |
| amount | query | Withdraw amount | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
