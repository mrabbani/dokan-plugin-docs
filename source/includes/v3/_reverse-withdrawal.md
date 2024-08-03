# /REVERSE-WITHDRAWAL/STORES-BALANCE
## ***GET*** 

### HTTP Request 
`***GET*** /reverse-withdrawal/stores-balance` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| vendor_id | query | Vendor ID to filter form | No |  |
| trn_date | query | Get transactions via date range | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REVERSE-WITHDRAWAL/VENDOR-DUE-STATUS
## ***GET*** 

### HTTP Request 
`***GET*** /reverse-withdrawal/vendor-due-status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor ID to filter form | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REVERSE-WITHDRAWAL/TRANSACTIONS
## ***GET*** 

### HTTP Request 
`***GET*** /reverse-withdrawal/transactions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| vendor_id | query | Vendor ID to filter form | Yes |  |
| trn_type | query | Transaction type to filter form | No |  |
| trn_date | query | Get transactions via date range | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /reverse-withdrawal/transactions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| trn_id | query | Transaction ID | No |  |
| trn_type | query | Transaction type | Yes |  |
| vendor_id | query | ID of the Store | Yes |  |
| note | query | Added note. | Yes |  |
| debit | query | Amount that site admin charged to store owner | No |  |
| credit | query | Amount that has been paid via store owner to site admin | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REVERSE-WITHDRAWAL/TRANSACTION-TYPES
## ***GET*** 

### HTTP Request 
`***GET*** /reverse-withdrawal/transaction-types` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REVERSE-WITHDRAWAL/STORES
## ***GET*** 

### HTTP Request 
`***GET*** /reverse-withdrawal/stores` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REVERSE-WITHDRAWAL/ADD-TO-CART
## ***POST*** 

### HTTP Request 
`***POST*** /reverse-withdrawal/add-to-cart` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| amount | query | Payable amount | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
