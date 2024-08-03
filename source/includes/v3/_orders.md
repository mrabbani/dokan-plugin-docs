# ORDERS
### ***GET*** 

### HTTP Request 
`***GET*** /orders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Order id to search order | No |  |
| seller_id | query | Orders belongs to specific seller | No |  |
| status | query | Order status. | No |  |
| date_created | query | The date the order was created, in the site's timezone. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ORDERS/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /orders/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Order id to search order | No |  |
| seller_id | query | Orders belongs to specific seller | No |  |
| status | query | Order status. | No |  |
| date_created | query | The date the order was created, in the site's timezone. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /orders/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Order Status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /orders/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Order Status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /orders/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Order Status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ORDERS/{ID}/NOTES
### ***GET*** 

### HTTP Request 
`***GET*** /orders/{id}/notes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Order id to search order | No |  |
| seller_id | query | Orders belongs to specific seller | No |  |
| status | query | Order status. | No |  |
| date_created | query | The date the order was created, in the site's timezone. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /orders/{id}/notes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| parent_id | query | Parent order ID. | No |  |
| seller_id | query | Orders belongs to specific seller | No |  |
| status | query | Order status. | No |  |
| currency | query | Currency the order was created with, in ISO format. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |
| search | query | Order id to search order | No |  |
| customer_note | query | Note left by customer during checkout. | No |  |
| billing | query | Billing address. | No |  |
| shipping | query | Shipping address. | No |  |
| payment_method | query | Payment method ID. | No |  |
| payment_method_title | query | Payment method title. | No |  |
| transaction_id | query | Unique transaction ID. | No |  |
| meta_data | query | Meta data. | No |  |
| line_items | query | Line items data. | No |  |
| shipping_lines | query | Shipping lines data. | No |  |
| fee_lines | query | Fee lines data. | No |  |
| coupon_lines | query | Coupons line data. | No |  |
| set_paid | query | Define if the order is paid. It will set the status to processing and reduce stock items. | No |  |
| note | query | Order note content. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ORDERS/{ID}/NOTES/{NOTE_ID}
### ***GET*** 

### HTTP Request 
`***GET*** /orders/{id}/notes/{note_id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| note_id | path | Unique identifier for the note object. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Order id to search order | No |  |
| seller_id | query | Orders belongs to specific seller | No |  |
| status | query | Order status. | No |  |
| date_created | query | The date the order was created, in the site's timezone. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /orders/{id}/notes/{note_id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| note_id | path | Unique identifier for the note object. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Order id to search order | No |  |
| seller_id | query | Orders belongs to specific seller | No |  |
| status | query | Order status. | No |  |
| date_created | query | The date the order was created, in the site's timezone. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /ORDERS/SUMMARY
### ***GET*** 

### HTTP Request 
`***GET*** /orders/summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Order id to search order | No |  |
| seller_id | query | Orders belongs to specific seller | No |  |
| status | query | Order status. | No |  |
| date_created | query | The date the order was created, in the site's timezone. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
