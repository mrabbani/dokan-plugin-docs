--- 

title: WordPress REST API - dokan/v1 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

API documentation for the dokan/v1 namespace 

**Version:** 1.0.0 

# /REVIEWS
## ***GET*** 

### HTTP Request 
`***GET*** /reviews` 

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

# /REVIEWS/SUMMARY
## ***GET*** 

### HTTP Request 
`***GET*** /reviews/summary` 

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

# /REVIEWS/{ID}
## ***POST*** 

### HTTP Request 
`***POST*** /reviews/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Review Status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /reviews/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Review Status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /reviews/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Review Status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/{PRODUCT_ID}/VARIATIONS
## ***GET*** 

### HTTP Request 
`***GET*** /products/{product_id}/variations` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Unique identifier for the variable product. | Yes |  |
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

## ***POST*** 

### HTTP Request 
`***POST*** /products/{product_id}/variations` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Unique identifier for the variable product. | Yes |  |
| description | query | Variation description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Variation regular price. | No |  |
| sale_price | query | Variation sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| visible | query | Define if the variation is visible on the product's page. | No |  |
| virtual | query | If the variation is virtual. | No |  |
| downloadable | query | If the variation is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at variation level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| weight | query | Variation weight (kg). | No |  |
| dimensions | query | Variation dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| image | query | Variation image data. | No |  |
| attributes | query | List of attributes. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/{PRODUCT_ID}/VARIATIONS/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /products/{product_id}/variations/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Unique identifier for the variable product. | Yes |  |
| id | path | Unique identifier for the variation. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /products/{product_id}/variations/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Unique identifier for the variable product. | Yes |  |
| id | path | Unique identifier for the variation. | Yes |  |
| description | query | Variation description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Variation regular price. | No |  |
| sale_price | query | Variation sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| visible | query | Define if the variation is visible on the product's page. | No |  |
| virtual | query | If the variation is virtual. | No |  |
| downloadable | query | If the variation is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at variation level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| weight | query | Variation weight (kg). | No |  |
| dimensions | query | Variation dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| image | query | Variation image data. | No |  |
| attributes | query | List of attributes. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/{product_id}/variations/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Unique identifier for the variable product. | Yes |  |
| id | path | Unique identifier for the variation. | Yes |  |
| description | query | Variation description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Variation regular price. | No |  |
| sale_price | query | Variation sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| visible | query | Define if the variation is visible on the product's page. | No |  |
| virtual | query | If the variation is virtual. | No |  |
| downloadable | query | If the variation is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at variation level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| weight | query | Variation weight (kg). | No |  |
| dimensions | query | Variation dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| image | query | Variation image data. | No |  |
| attributes | query | List of attributes. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/{product_id}/variations/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Unique identifier for the variable product. | Yes |  |
| id | path | Unique identifier for the variation. | Yes |  |
| description | query | Variation description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Variation regular price. | No |  |
| sale_price | query | Variation sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| visible | query | Define if the variation is visible on the product's page. | No |  |
| virtual | query | If the variation is virtual. | No |  |
| downloadable | query | If the variation is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at variation level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| weight | query | Variation weight (kg). | No |  |
| dimensions | query | Variation dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| image | query | Variation image data. | No |  |
| attributes | query | List of attributes. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /products/{product_id}/variations/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Unique identifier for the variable product. | Yes |  |
| id | path | Unique identifier for the variation. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/{PRODUCT_ID}/VARIATIONS/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /products/{product_id}/variations/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Product ID for which variations will be managed. | Yes |  |
| description | query | Variation description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Variation regular price. | No |  |
| sale_price | query | Variation sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| visible | query | Define if the variation is visible on the product's page. | No |  |
| virtual | query | If the variation is virtual. | No |  |
| downloadable | query | If the variation is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at variation level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| weight | query | Variation weight (kg). | No |  |
| dimensions | query | Variation dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| image | query | Variation image data. | No |  |
| attributes | query | List of attributes. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/{product_id}/variations/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Product ID for which variations will be managed. | Yes |  |
| description | query | Variation description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Variation regular price. | No |  |
| sale_price | query | Variation sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| visible | query | Define if the variation is visible on the product's page. | No |  |
| virtual | query | If the variation is virtual. | No |  |
| downloadable | query | If the variation is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at variation level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| weight | query | Variation weight (kg). | No |  |
| dimensions | query | Variation dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| image | query | Variation image data. | No |  |
| attributes | query | List of attributes. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/{product_id}/variations/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | path | Product ID for which variations will be managed. | Yes |  |
| description | query | Variation description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Variation regular price. | No |  |
| sale_price | query | Variation sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| visible | query | Define if the variation is visible on the product's page. | No |  |
| virtual | query | If the variation is virtual. | No |  |
| downloadable | query | If the variation is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at variation level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| weight | query | Variation weight (kg). | No |  |
| dimensions | query | Variation dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| image | query | Variation image data. | No |  |
| attributes | query | List of attributes. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES/{ID}/STATS
## ***GET*** 

### HTTP Request 
`***GET*** /stores/{id}/stats` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
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

# /STORES/{ID}/EMAIL
## ***POST*** 

### HTTP Request 
`***POST*** /stores/{id}/email` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| subject | query | Subject of the email. | Yes |  |
| body | query | Body of the email. | Yes |  |
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

# /STORES/CURRENT-VISITOR
## ***GET*** 

### HTTP Request 
`***GET*** /stores/current-visitor` 

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

# /ADMIN/MODULES
## ***GET*** 

### HTTP Request 
`***GET*** /admin/modules` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/MODULES/ACTIVATE
## ***POST*** 

### HTTP Request 
`***POST*** /admin/modules/activate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| module | query | Basename of the module as array | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /admin/modules/activate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| module | query | Basename of the module as array | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /admin/modules/activate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| module | query | Basename of the module as array | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/MODULES/DEACTIVATE
## ***POST*** 

### HTTP Request 
`***POST*** /admin/modules/deactivate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| module | query | Basename of the module as array | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /admin/modules/deactivate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| module | query | Basename of the module as array | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /admin/modules/deactivate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| module | query | Basename of the module as array | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
