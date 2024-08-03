# COUPONS
## /COUPONS
### ***GET*** 

### HTTP Request 
`***GET*** /coupons` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| code | query | Limit result set to resources with a specific code. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /coupons` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| code | query | Coupon code. | Yes |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | No |  |
| discount_type | query | Determines the type of discount that will be applied. | No |  |
| description | query | Coupon description. | No |  |
| date_expires | query | The date the coupon expires, in the site's timezone. | No |  |
| date_expires_gmt | query | The date the coupon expires, as GMT. | No |  |
| individual_use | query | If true, the coupon can only be used individually. Other applied coupons will be removed from the cart. | No |  |
| product_ids | query | List of product IDs the coupon can be used on. | No |  |
| excluded_product_ids | query | List of product IDs the coupon cannot be used on. | No |  |
| usage_limit | query | How many times the coupon can be used in total. | No |  |
| usage_limit_per_user | query | How many times the coupon can be used per customer. | No |  |
| limit_usage_to_x_items | query | Max number of items in the cart the coupon can be applied to. | No |  |
| free_shipping | query | If true and if the free shipping method requires a coupon, this coupon will enable free shipping. | No |  |
| product_categories | query | List of category IDs the coupon applies to. | No |  |
| excluded_product_categories | query | List of category IDs the coupon does not apply to. | No |  |
| exclude_sale_items | query | If true, this coupon will not be applied to items that have sale prices. | No |  |
| minimum_amount | query | Minimum order amount that needs to be in the cart before coupon applies. | No |  |
| maximum_amount | query | Maximum order amount allowed when using the coupon. | No |  |
| email_restrictions | query | List of email addresses that can use this coupon. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /COUPONS/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /coupons/{id}` 

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
`***POST*** /coupons/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| code | query | Coupon code. | No |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | No |  |
| discount_type | query | Determines the type of discount that will be applied. | No |  |
| description | query | Coupon description. | No |  |
| date_expires | query | The date the coupon expires, in the site's timezone. | No |  |
| date_expires_gmt | query | The date the coupon expires, as GMT. | No |  |
| individual_use | query | If true, the coupon can only be used individually. Other applied coupons will be removed from the cart. | No |  |
| product_ids | query | List of product IDs the coupon can be used on. | No |  |
| excluded_product_ids | query | List of product IDs the coupon cannot be used on. | No |  |
| usage_limit | query | How many times the coupon can be used in total. | No |  |
| usage_limit_per_user | query | How many times the coupon can be used per customer. | No |  |
| limit_usage_to_x_items | query | Max number of items in the cart the coupon can be applied to. | No |  |
| free_shipping | query | If true and if the free shipping method requires a coupon, this coupon will enable free shipping. | No |  |
| product_categories | query | List of category IDs the coupon applies to. | No |  |
| excluded_product_categories | query | List of category IDs the coupon does not apply to. | No |  |
| exclude_sale_items | query | If true, this coupon will not be applied to items that have sale prices. | No |  |
| minimum_amount | query | Minimum order amount that needs to be in the cart before coupon applies. | No |  |
| maximum_amount | query | Maximum order amount allowed when using the coupon. | No |  |
| email_restrictions | query | List of email addresses that can use this coupon. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /coupons/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| code | query | Coupon code. | No |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | No |  |
| discount_type | query | Determines the type of discount that will be applied. | No |  |
| description | query | Coupon description. | No |  |
| date_expires | query | The date the coupon expires, in the site's timezone. | No |  |
| date_expires_gmt | query | The date the coupon expires, as GMT. | No |  |
| individual_use | query | If true, the coupon can only be used individually. Other applied coupons will be removed from the cart. | No |  |
| product_ids | query | List of product IDs the coupon can be used on. | No |  |
| excluded_product_ids | query | List of product IDs the coupon cannot be used on. | No |  |
| usage_limit | query | How many times the coupon can be used in total. | No |  |
| usage_limit_per_user | query | How many times the coupon can be used per customer. | No |  |
| limit_usage_to_x_items | query | Max number of items in the cart the coupon can be applied to. | No |  |
| free_shipping | query | If true and if the free shipping method requires a coupon, this coupon will enable free shipping. | No |  |
| product_categories | query | List of category IDs the coupon applies to. | No |  |
| excluded_product_categories | query | List of category IDs the coupon does not apply to. | No |  |
| exclude_sale_items | query | If true, this coupon will not be applied to items that have sale prices. | No |  |
| minimum_amount | query | Minimum order amount that needs to be in the cart before coupon applies. | No |  |
| maximum_amount | query | Maximum order amount allowed when using the coupon. | No |  |
| email_restrictions | query | List of email addresses that can use this coupon. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /coupons/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| code | query | Coupon code. | No |  |
| amount | query | The amount of discount. Should always be numeric, even if setting a percentage. | No |  |
| discount_type | query | Determines the type of discount that will be applied. | No |  |
| description | query | Coupon description. | No |  |
| date_expires | query | The date the coupon expires, in the site's timezone. | No |  |
| date_expires_gmt | query | The date the coupon expires, as GMT. | No |  |
| individual_use | query | If true, the coupon can only be used individually. Other applied coupons will be removed from the cart. | No |  |
| product_ids | query | List of product IDs the coupon can be used on. | No |  |
| excluded_product_ids | query | List of product IDs the coupon cannot be used on. | No |  |
| usage_limit | query | How many times the coupon can be used in total. | No |  |
| usage_limit_per_user | query | How many times the coupon can be used per customer. | No |  |
| limit_usage_to_x_items | query | Max number of items in the cart the coupon can be applied to. | No |  |
| free_shipping | query | If true and if the free shipping method requires a coupon, this coupon will enable free shipping. | No |  |
| product_categories | query | List of category IDs the coupon applies to. | No |  |
| excluded_product_categories | query | List of category IDs the coupon does not apply to. | No |  |
| exclude_sale_items | query | If true, this coupon will not be applied to items that have sale prices. | No |  |
| minimum_amount | query | Minimum order amount that needs to be in the cart before coupon applies. | No |  |
| maximum_amount | query | Maximum order amount allowed when using the coupon. | No |  |
| email_restrictions | query | List of email addresses that can use this coupon. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /coupons/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
