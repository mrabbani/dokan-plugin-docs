# /PRODUCT_ADV
## ***GET*** 

### HTTP Request 
`***GET*** /product_adv` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| vendor_id | query | Vendor IDs to filter form | No |  |
| product_id | query | Product IDs to filter form | No |  |
| order_id | query | Order IDs to filter form | No |  |
| status | query | Advertised product status, 0 to get all status, 1 for active advertisements and 2 for inactive advertisements | No |  |
| expires_at | query | Get advertised products by their expire date | No |  |
| created_via | query | Filter how advertisement was created | No |  |
| return | query | How data will be returned | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCT_ADV/{ID}/EXPIRE
## ***POST*** 

### HTTP Request 
`***POST*** /product_adv/{id}/expire` 

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

## ***PUT*** 

### HTTP Request 
`***PUT*** /product_adv/{id}/expire` 

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

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /product_adv/{id}/expire` 

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

# /PRODUCT_ADV/{ID}
## ***DELETE*** 

### HTTP Request 
`***DELETE*** /product_adv/{id}` 

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

# /PRODUCT_ADV/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /product_adv/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| action | query | Batch action name to process | Yes |  |
| ids | query | Batch action to carry on advertisement items | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /product_adv/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| action | query | Batch action name to process | Yes |  |
| ids | query | Batch action to carry on advertisement items | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /product_adv/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| action | query | Batch action name to process | Yes |  |
| ids | query | Batch action to carry on advertisement items | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCT_ADV/STORES
## ***GET*** 

### HTTP Request 
`***GET*** /product_adv/stores` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCT_ADV/CREATE
## ***POST*** 

### HTTP Request 
`***POST*** /product_adv/create` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | query | To be advertise product id. | Yes |  |
| vendor_id | query | Vendor of the product. | Yes |  |
| reverse_withdrawal_entry | query | Add Reverse Withdrawal Entry. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
