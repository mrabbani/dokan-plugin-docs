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

# /ADMIN
## ***GET*** 

### HTTP Request 
`***GET*** /admin` 

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

# /ADMIN/REPORT/SUMMARY
## ***GET*** 

### HTTP Request 
`***GET*** /admin/report/summary` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/REPORT/OVERVIEW
## ***GET*** 

### HTTP Request 
`***GET*** /admin/report/overview` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/DASHBOARD/FEED
## ***GET*** 

### HTTP Request 
`***GET*** /admin/dashboard/feed` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| items | query | Number of feed item | No |  |
| show_summary | query | Flag for showing summary | No |  |
| show_author | query | Flag for showing author | No |  |
| show_date | query | Flag for showing date | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/HELP
## ***GET*** 

### HTTP Request 
`***GET*** /admin/help` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES
## ***GET*** 

### HTTP Request 
`***GET*** /stores` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| status | query | Status of the store | No |  |
| orderby | query | Store List Order By | No |  |
| order | query | Store List Order | No |  |
| featured | query | Store List Order | No |  |
| store_categories | query | Store categories | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /stores` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /stores/{id}` 

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

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /stores/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| reassign | query | Reassign the deleted user's posts and links to this user ID. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /stores/{id}` 

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
`***PUT*** /stores/{id}` 

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
`***PATCH*** /stores/{id}` 

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

# /STORES/{ID}/PRODUCTS
## ***GET*** 

### HTTP Request 
`***GET*** /stores/{id}/products` 

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

# /STORES/{ID}/REVIEWS
## ***GET*** 

### HTTP Request 
`***GET*** /stores/{id}/reviews` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /stores/{id}/reviews` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| title | query | Review title. | Yes |  |
| content | query | Review content. | Yes |  |
| rating | query | Review rating | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES/CHECK
## ***GET*** 

### HTTP Request 
`***GET*** /stores/check` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES/{ID}/CONTACT
## ***POST*** 

### HTTP Request 
`***POST*** /stores/{id}/contact` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| name | query | Your Name | Yes |  |
| email | query | Your email | Yes |  |
| message | query | Your Message | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES/{ID}/STATUS
## ***POST*** 

### HTTP Request 
`***POST*** /stores/{id}/status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Status for the store object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /stores/{id}/status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Status for the store object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /stores/{id}/status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Status for the store object. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /stores/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /stores/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /stores/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORES/{ID}/CATEGORIES
## ***GET*** 

### HTTP Request 
`***GET*** /stores/{id}/categories` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| best_selling | query | Get Best Selling Products Category. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS
## ***GET*** 

### HTTP Request 
`***GET*** /products` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query | Unique identifier for the object. | No |  |
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
`***POST*** /products` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query | Unique identifier for the object. | No |  |
| name | query | Product name. | No |  |
| slug | query | Product slug. | No |  |
| type | query | Product type. | No |  |
| status | query | Product status (post status). | No |  |
| featured | query | Featured product. | No |  |
| catalog_visibility | query | Catalog visibility. | No |  |
| description | query | Product description. | No |  |
| short_description | query | Product short description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Product regular price. | No |  |
| sale_price | query | Product sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| virtual | query | If the product is virtual. | No |  |
| downloadable | query | If the product is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| external_url | query | Product external URL. Only for external products. | No |  |
| button_text | query | Product external button text. Only for external products. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at product level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| sold_individually | query | Allow one item to be bought in a single order. | No |  |
| weight | query | Product weight (kg). | No |  |
| dimensions | query | Product dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| reviews_allowed | query | Allow reviews. | No |  |
| upsell_ids | query | List of up-sell products IDs. | No |  |
| cross_sell_ids | query | List of cross-sell products IDs. | No |  |
| parent_id | query | Product parent ID. | No |  |
| purchase_note | query | Optional note to send the customer after purchase. | No |  |
| categories | query | List of categories. | No |  |
| tags | query | List of tags. | No |  |
| images | query | List of images. | No |  |
| attributes | query | List of attributes. | No |  |
| default_attributes | query | Defaults variation attributes. | No |  |
| grouped_products | query | List of grouped products ID. | No |  |
| menu_order | query | Menu order, used to custom sort products. | No |  |
| meta_data | query | Meta data. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /products/{id}` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /products/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| name | query | Product name. | No |  |
| slug | query | Product slug. | No |  |
| type | query | Product type. | No |  |
| status | query | Product status (post status). | No |  |
| featured | query | Featured product. | No |  |
| catalog_visibility | query | Catalog visibility. | No |  |
| description | query | Product description. | No |  |
| short_description | query | Product short description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Product regular price. | No |  |
| sale_price | query | Product sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| virtual | query | If the product is virtual. | No |  |
| downloadable | query | If the product is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| external_url | query | Product external URL. Only for external products. | No |  |
| button_text | query | Product external button text. Only for external products. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at product level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| sold_individually | query | Allow one item to be bought in a single order. | No |  |
| weight | query | Product weight (kg). | No |  |
| dimensions | query | Product dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| reviews_allowed | query | Allow reviews. | No |  |
| upsell_ids | query | List of up-sell products IDs. | No |  |
| cross_sell_ids | query | List of cross-sell products IDs. | No |  |
| parent_id | query | Product parent ID. | No |  |
| purchase_note | query | Optional note to send the customer after purchase. | No |  |
| categories | query | List of categories. | No |  |
| tags | query | List of tags. | No |  |
| images | query | List of images. | No |  |
| attributes | query | List of attributes. | No |  |
| default_attributes | query | Defaults variation attributes. | No |  |
| grouped_products | query | List of grouped products ID. | No |  |
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
`***PUT*** /products/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| name | query | Product name. | No |  |
| slug | query | Product slug. | No |  |
| type | query | Product type. | No |  |
| status | query | Product status (post status). | No |  |
| featured | query | Featured product. | No |  |
| catalog_visibility | query | Catalog visibility. | No |  |
| description | query | Product description. | No |  |
| short_description | query | Product short description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Product regular price. | No |  |
| sale_price | query | Product sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| virtual | query | If the product is virtual. | No |  |
| downloadable | query | If the product is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| external_url | query | Product external URL. Only for external products. | No |  |
| button_text | query | Product external button text. Only for external products. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at product level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| sold_individually | query | Allow one item to be bought in a single order. | No |  |
| weight | query | Product weight (kg). | No |  |
| dimensions | query | Product dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| reviews_allowed | query | Allow reviews. | No |  |
| upsell_ids | query | List of up-sell products IDs. | No |  |
| cross_sell_ids | query | List of cross-sell products IDs. | No |  |
| parent_id | query | Product parent ID. | No |  |
| purchase_note | query | Optional note to send the customer after purchase. | No |  |
| categories | query | List of categories. | No |  |
| tags | query | List of tags. | No |  |
| images | query | List of images. | No |  |
| attributes | query | List of attributes. | No |  |
| default_attributes | query | Defaults variation attributes. | No |  |
| grouped_products | query | List of grouped products ID. | No |  |
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
`***PATCH*** /products/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| name | query | Product name. | No |  |
| slug | query | Product slug. | No |  |
| type | query | Product type. | No |  |
| status | query | Product status (post status). | No |  |
| featured | query | Featured product. | No |  |
| catalog_visibility | query | Catalog visibility. | No |  |
| description | query | Product description. | No |  |
| short_description | query | Product short description. | No |  |
| sku | query | Unique identifier. | No |  |
| regular_price | query | Product regular price. | No |  |
| sale_price | query | Product sale price. | No |  |
| date_on_sale_from | query | Start date of sale price, in the site's timezone. | No |  |
| date_on_sale_from_gmt | query | Start date of sale price, as GMT. | No |  |
| date_on_sale_to | query | End date of sale price, in the site's timezone. | No |  |
| date_on_sale_to_gmt | query | End date of sale price, as GMT. | No |  |
| virtual | query | If the product is virtual. | No |  |
| downloadable | query | If the product is downloadable. | No |  |
| downloads | query | List of downloadable files. | No |  |
| download_limit | query | Number of times downloadable files can be downloaded after purchase. | No |  |
| download_expiry | query | Number of days until access to downloadable files expires. | No |  |
| external_url | query | Product external URL. Only for external products. | No |  |
| button_text | query | Product external button text. Only for external products. | No |  |
| tax_status | query | Tax status. | No |  |
| tax_class | query | Tax class. | No |  |
| manage_stock | query | Stock management at product level. | No |  |
| stock_quantity | query | Stock quantity. | No |  |
| in_stock | query | Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend. | No |  |
| backorders | query | If managing stock, this controls if backorders are allowed. | No |  |
| sold_individually | query | Allow one item to be bought in a single order. | No |  |
| weight | query | Product weight (kg). | No |  |
| dimensions | query | Product dimensions. | No |  |
| shipping_class | query | Shipping class slug. | No |  |
| reviews_allowed | query | Allow reviews. | No |  |
| upsell_ids | query | List of up-sell products IDs. | No |  |
| cross_sell_ids | query | List of cross-sell products IDs. | No |  |
| parent_id | query | Product parent ID. | No |  |
| purchase_note | query | Optional note to send the customer after purchase. | No |  |
| categories | query | List of categories. | No |  |
| tags | query | List of tags. | No |  |
| images | query | List of images. | No |  |
| attributes | query | List of attributes. | No |  |
| default_attributes | query | Defaults variation attributes. | No |  |
| grouped_products | query | List of grouped products ID. | No |  |
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
`***DELETE*** /products/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| force | query | Whether to bypass trash and force deletion. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/SUMMARY
## ***GET*** 

### HTTP Request 
`***GET*** /products/summary` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/{ID}/RELATED
## ***GET*** 

### HTTP Request 
`***GET*** /products/{id}/related` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| per_page | query | Number of product you want to get top rated product | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/TOP_RATED
## ***GET*** 

### HTTP Request 
`***GET*** /products/top_rated` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| per_page | query | Number of product you want to get top rated product | No |  |
| page | query | Number of page number | No |  |
| seller_id | query | Top rated product for specific vendor | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/BEST_SELLING
## ***GET*** 

### HTTP Request 
`***GET*** /products/best_selling` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| per_page | query | Number of product you want to get top rated product | No |  |
| page | query | Number of page number | No |  |
| seller_id | query | Top rated product for specific vendor | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/FEATURED
## ***GET*** 

### HTTP Request 
`***GET*** /products/featured` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| per_page | query | Number of product you want to get top rated product | No |  |
| page | query | Number of page number | No |  |
| seller_id | query | Top rated product for specific vendor | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/LATEST
## ***GET*** 

### HTTP Request 
`***GET*** /products/latest` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| per_page | query | Number of product you want to get top rated product | No |  |
| page | query | Number of page number | No |  |
| seller_id | query | Top rated product for specific vendor | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/MULTISTEP-CATEGORIES
## ***GET*** 

### HTTP Request 
`***GET*** /products/multistep-categories` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES
## ***GET*** 

### HTTP Request 
`***GET*** /products/attributes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| name | query | Name for the resource. | Yes |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| type | query | Type of attribute. | No |  |
| order_by | query | Default sort order. | No |  |
| has_archives | query | Enable/Disable attribute archives. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /products/attributes/{id}` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| name | query | Attribute name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| type | query | Type of attribute. | No |  |
| order_by | query | Default sort order. | No |  |
| has_archives | query | Enable/Disable attribute archives. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/attributes/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| name | query | Attribute name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| type | query | Type of attribute. | No |  |
| order_by | query | Default sort order. | No |  |
| has_archives | query | Enable/Disable attribute archives. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/attributes/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| name | query | Attribute name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| type | query | Type of attribute. | No |  |
| order_by | query | Default sort order. | No |  |
| has_archives | query | Enable/Disable attribute archives. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /products/attributes/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| force | query | Required to be true, as resource does not support trashing. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| name | query | Attribute name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| type | query | Type of attribute. | No |  |
| order_by | query | Default sort order. | No |  |
| has_archives | query | Enable/Disable attribute archives. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/attributes/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| name | query | Attribute name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| type | query | Type of attribute. | No |  |
| order_by | query | Default sort order. | No |  |
| has_archives | query | Enable/Disable attribute archives. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/attributes/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| name | query | Attribute name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| type | query | Type of attribute. | No |  |
| order_by | query | Default sort order. | No |  |
| has_archives | query | Enable/Disable attribute archives. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES/EDIT-PRODUCT/{ID}
## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes/edit-product/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attributes | query | Attribute options. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/attributes/edit-product/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attributes | query | Attribute options. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/attributes/edit-product/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attributes | query | Attribute options. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES/SET-DEFAULT/{ID}
## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes/set-default/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attributes | query | Attribute options. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/attributes/set-default/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attributes | query | Attribute options. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/attributes/set-default/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attributes | query | Attribute options. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES/{ATTRIBUTE_ID}/TERMS
## ***GET*** 

### HTTP Request 
`***GET*** /products/attributes/{attribute_id}/terms` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| exclude | query | Ensure result set excludes specific IDs. | No |  |
| include | query | Limit result set to specific ids. | No |  |
| offset | query | Offset the result set by a specific number of items. Applies to hierarchical taxonomies only. | No |  |
| order | query | Order sort attribute ascending or descending. | No |  |
| orderby | query | Sort collection by resource attribute. | No |  |
| hide_empty | query | Whether to hide resources not assigned to any products. | No |  |
| parent | query | Limit result set to resources assigned to a specific parent. Applies to hierarchical taxonomies only. | No |  |
| product | query | Limit result set to resources assigned to a specific product. | No |  |
| slug | query | Limit result set to resources with a specific slug. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes/{attribute_id}/terms` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| name | query | Name for the resource. | Yes |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| description | query | HTML description of the resource. | No |  |
| menu_order | query | Menu order, used to custom sort the resource. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES/{ATTRIBUTE_ID}/TERMS/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /products/attributes/{attribute_id}/terms/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes/{attribute_id}/terms/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| name | query | Term name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| description | query | HTML description of the resource. | No |  |
| menu_order | query | Menu order, used to custom sort the resource. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/attributes/{attribute_id}/terms/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| name | query | Term name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| description | query | HTML description of the resource. | No |  |
| menu_order | query | Menu order, used to custom sort the resource. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/attributes/{attribute_id}/terms/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| name | query | Term name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| description | query | HTML description of the resource. | No |  |
| menu_order | query | Menu order, used to custom sort the resource. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /products/attributes/{attribute_id}/terms/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the resource. | Yes |  |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| force | query | Required to be true, as resource does not support trashing. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /PRODUCTS/ATTRIBUTES/{ATTRIBUTE_ID}/TERMS/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /products/attributes/{attribute_id}/terms/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| name | query | Term name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| description | query | HTML description of the resource. | No |  |
| menu_order | query | Menu order, used to custom sort the resource. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /products/attributes/{attribute_id}/terms/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| name | query | Term name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| description | query | HTML description of the resource. | No |  |
| menu_order | query | Menu order, used to custom sort the resource. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /products/attributes/{attribute_id}/terms/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| attribute_id | path | Unique identifier for the attribute of the terms. | Yes |  |
| name | query | Term name. | No |  |
| slug | query | An alphanumeric identifier for the resource unique to its type. | No |  |
| description | query | HTML description of the resource. | No |  |
| menu_order | query | Menu order, used to custom sort the resource. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ORDERS
## ***GET*** 

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

# /ORDERS/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /ORDERS/{ID}/NOTES
## ***GET*** 

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

## ***POST*** 

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

# /ORDERS/{ID}/NOTES/{NOTE_ID}
## ***GET*** 

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

## ***DELETE*** 

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

# /ORDERS/SUMMARY
## ***GET*** 

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

# /WITHDRAW
## ***GET*** 

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

## ***POST*** 

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

# /WITHDRAW/BALANCE
## ***GET*** 

### HTTP Request 
`***GET*** /withdraw/balance` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /WITHDRAW/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /WITHDRAW/PAYMENT_METHODS
## ***GET*** 

### HTTP Request 
`***GET*** /withdraw/payment_methods` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /WITHDRAW/BATCH
## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /WITHDRAW/CHARGES
## ***GET*** 

### HTTP Request 
`***GET*** /withdraw/charges` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /WITHDRAW/CHARGE
## ***GET*** 

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

# /SETTINGS
## ***GET*** 

### HTTP Request 
`***GET*** /settings` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /settings` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /settings` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /settings` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/NOTICES/ADMIN
## ***GET*** 

### HTTP Request 
`***GET*** /admin/notices/admin` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/NOTICES/PROMO
## ***GET*** 

### HTTP Request 
`***GET*** /admin/notices/promo` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/CHANGELOG/LITE
## ***GET*** 

### HTTP Request 
`***GET*** /admin/changelog/lite` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /DUMMY-DATA/STATUS
## ***GET*** 

### HTTP Request 
`***GET*** /dummy-data/status` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /DUMMY-DATA/IMPORT
## ***POST*** 

### HTTP Request 
`***POST*** /dummy-data/import` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_products | query | Vendors products data. | Yes |  |
| vendor_data | query | Vendors profile data. | Yes |  |
| vendor_index | query | Vendor item index to import. | No |  |
| total_vendors | query | Total vendors | No |  |
| result | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /DUMMY-DATA/CLEAR
## ***DELETE*** 

### HTTP Request 
`***DELETE*** /dummy-data/clear` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-DASHBOARD
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-dashboard` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-DASHBOARD/PROFILE
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-dashboard/profile` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-DASHBOARD/SALES
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-dashboard/sales` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| from | query | From Date | No |  |
| to | query | To Date | No |  |
| filter_range | query | Returns all sales reports if true | No |  |
| group_by | query | Group By | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-DASHBOARD/PRODUCTS
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-dashboard/products` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-DASHBOARD/ORDERS
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-dashboard/orders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| customer_id | query | User ID who owns the order. 0 for guests. | No |  |
| after | query | Start date to show orders | No |  |
| before | query | End date to show orders | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-DASHBOARD/PREFERENCES
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-dashboard/preferences` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /BLOCKS/PRODUCTS/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /blocks/products/{id}` 

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

# /STORE-CATEGORIES
## ***GET*** 

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

## ***POST*** 

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

# /STORE-CATEGORIES/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /STORE-CATEGORIES/DEFAULT-CATEGORY
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /COUPONS
## ***GET*** 

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

## ***POST*** 

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

# /COUPONS/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /REPORTS/SALES_OVERVIEW
## ***GET*** 

### HTTP Request 
`***GET*** /reports/sales_overview` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | ID of the Store | No |  |
| start_date | query |  | No |  |
| end_date | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REPORTS/TOP_SELLING
## ***GET*** 

### HTTP Request 
`***GET*** /reports/top_selling` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | ID of the Store | No |  |
| start_date | query |  | No |  |
| end_date | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REPORTS/TOP_EARNERS
## ***GET*** 

### HTTP Request 
`***GET*** /reports/top_earners` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | ID of the Store | No |  |
| start_date | query |  | No |  |
| end_date | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REPORTS/SUMMARY
## ***GET*** 

### HTTP Request 
`***GET*** /reports/summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | ID of the Store | No |  |
| start_date | query |  | No |  |
| end_date | query |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

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

# /ANNOUNCEMENT
## ***GET*** 

### HTTP Request 
`***GET*** /announcement` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| vendor_id | query | If set, specified vendor announcement will be returned. | No |  |
| status | query | Announcement status, this is a admin only feature | No |  |
| read_status | query | Announcement read status, this is a vendor only feature | No |  |
| from | query | Announcement date time from | No |  |
| to | query | Announcement date time to | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /announcement` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| notice_id | query | If returning a single notice, notice id will be available . | No |  |
| status | query | Status of the announcement | No |  |
| read_status | query | Vendor read status of the single notice | No |  |
| announcement_type | query | Send announcement to: this is a admin only field | No |  |
| announcement_sellers | query | Send announcement to: this is a admin only field | No |  |
| sender_ids | query | Send announcement to: this is a admin only field | No |  |
| exclude_seller_ids | query | Exclude seller ids | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ANNOUNCEMENT/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /announcement/{id}` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /announcement/{id}` 

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
`***PUT*** /announcement/{id}` 

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
`***PATCH*** /announcement/{id}` 

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

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /announcement/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| force | query | Force delete announcement. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ANNOUNCEMENT/{ID}/RESTORE
## ***POST*** 

### HTTP Request 
`***POST*** /announcement/{id}/restore` 

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
`***PUT*** /announcement/{id}/restore` 

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
`***PATCH*** /announcement/{id}/restore` 

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

# /ANNOUNCEMENT/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /announcement/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| trash | query | Batch trash announcements. | No |  |
| delete | query | Batch delete announcements. | No |  |
| restore | query | Batch untrash announcements. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /announcement/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| trash | query | Batch trash announcements. | No |  |
| delete | query | Batch delete announcements. | No |  |
| restore | query | Batch untrash announcements. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /announcement/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| trash | query | Batch trash announcements. | No |  |
| delete | query | Batch delete announcements. | No |  |
| restore | query | Batch untrash announcements. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ANNOUNCEMENT/NOTICE/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /announcement/notice/{id}` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /announcement/notice/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| read_status | query | Announcement read status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /announcement/notice/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| read_status | query | Announcement read status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /announcement/notice/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| read_status | query | Announcement read status | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /announcement/notice/{id}` 

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

# /ADMIN/LOGS
## ***GET*** 

### HTTP Request 
`***GET*** /admin/logs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| vendor_id | query | Vendor IDs to filter form | No |  |
| order_id | query | Order IDs to filter form | No |  |
| order_status | query | Order status to filter form | No |  |
| orderby | query | Filter by column | No |  |
| order | query | Order by type | No |  |
| return | query | How data will be returned | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/LOGS/EXPORT
## ***GET*** 

### HTTP Request 
`***GET*** /admin/logs/export` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| vendor_id | query | Vendor IDs to filter form | No |  |
| order_id | query | Order IDs to filter form | No |  |
| order_status | query | Order status to filter form | No |  |
| orderby | query | Filter by column | No |  |
| order | query | Order by type | No |  |
| return | query | How data will be returned | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REFUNDS
## ***GET*** 

### HTTP Request 
`***GET*** /refunds` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Search by order id OR shop name | No |  |
| status | query | Refund status | No |  |
| orderby | query | Order By | No |  |
| order | query | Order | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REFUNDS/{ID}/APPROVE
## ***POST*** 

### HTTP Request 
`***POST*** /refunds/{id}/approve` 

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
`***PUT*** /refunds/{id}/approve` 

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
`***PATCH*** /refunds/{id}/approve` 

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

# /REFUNDS/{ID}/CANCEL
## ***POST*** 

### HTTP Request 
`***POST*** /refunds/{id}/cancel` 

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
`***PUT*** /refunds/{id}/cancel` 

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
`***PATCH*** /refunds/{id}/cancel` 

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

# /REFUNDS/{ID}
## ***DELETE*** 

### HTTP Request 
`***DELETE*** /refunds/{id}` 

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

# /REFUNDS/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /refunds/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| completed | query | List of refund IDs to be completed | No |  |
| cancelled | query | List of refund IDs to be cancelled | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /refunds/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| completed | query | List of refund IDs to be completed | No |  |
| cancelled | query | List of refund IDs to be cancelled | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /refunds/batch` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| completed | query | List of refund IDs to be completed | No |  |
| cancelled | query | List of refund IDs to be cancelled | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/CHANGELOG/PRO
## ***GET*** 

### HTTP Request 
`***GET*** /admin/changelog/pro` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-DASHBOARD/PROFILE-PROGRESSBAR
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-dashboard/profile-progressbar` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /BLOCKS/PRODUCT-VARIATION/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /blocks/product-variation/{id}` 

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

# /FOLLOW-STORE
## ***GET*** 

### HTTP Request 
`***GET*** /follow-store` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| vendor_id | query | Vendor id to check if user is following that vendor | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /follow-store` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| vendor_id | query | Vendor id to follow or unfollow | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /FOLLOW-STORE/FOLLOWERS
## ***GET*** 

### HTTP Request 
`***GET*** /follow-store/followers` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| vendor_id | query | Vendor id follow/unfollow | No |  |
| search | query | search followers | No |  |
| order | query | order parameter | No |  |
| orderby | query | order by parameter | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ABUSE-REPORTS
## ***GET*** 

### HTTP Request 
`***GET*** /abuse-reports` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ABUSE-REPORTS/{ID}
## ***DELETE*** 

### HTTP Request 
`***DELETE*** /abuse-reports/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Abuse report id | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ABUSE-REPORTS/BATCH
## ***DELETE*** 

### HTTP Request 
`***DELETE*** /abuse-reports/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ABUSE-REPORTS/ABUSE-REASONS
## ***GET*** 

### HTTP Request 
`***GET*** /abuse-reports/abuse-reasons` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /SPMV-PRODUCT/SETTINGS
## ***GET*** 

### HTTP Request 
`***GET*** /spmv-product/settings` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /SPMV-PRODUCT/SEARCH
## ***GET*** 

### HTTP Request 
`***GET*** /spmv-product/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| search | query | Limit results to those matching a string. | No |  |
| orderby | query | Sort by products. | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /SPMV-PRODUCT/ADD-TO-STORE
## ***POST*** 

### HTTP Request 
`***POST*** /spmv-product/add-to-store` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| product_id | query | Product id | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /STORE-REVIEWS
## ***GET*** 

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

# /STORE-REVIEWS/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /STORE-REVIEWS/{ID}/RESTORE
## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /STORE-REVIEWS/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /store-reviews/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /store-reviews/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /store-reviews/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/SUPPORT-TICKET
## ***GET*** 

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

# /ADMIN/SUPPORT-TICKET/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /admin/support-ticket/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /admin/support-ticket/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /admin/support-ticket/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/SUPPORT-TICKET/CUSTOMERS
## ***GET*** 

### HTTP Request 
`***GET*** /admin/support-ticket/customers` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /ADMIN/SUPPORT-TICKET/{ID}
## ***GET*** 

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

## ***POST*** 

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

# /ADMIN/SUPPORT-TICKET/{ID}/STATUS
## ***POST*** 

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

# /ADMIN/SUPPORT-TICKET/{ID}/COMMENT
## ***DELETE*** 

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

# /ADMIN/SUPPORT-TICKET/{ID}/EMAIL-NOTIFICATION
## ***POST*** 

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

# /VENDOR-STAFF
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-staff` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /vendor-staff` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | query | Login name for the user. | No |  |
| name | query | Display name for the user. | No |  |
| first_name | query | First name for the user. | No |  |
| last_name | query | Last name for the user. | No |  |
| phone | query | Phone number for the user. | No |  |
| email | query | The email address for the user. | Yes |  |
| nickname | query | The nickname for the user. | No |  |
| password | query | Password for the user (never included). | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-STAFF/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-staff/{id}` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /vendor-staff/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | query | Login name for the user. | No |  |
| name | query | Display name for the user. | No |  |
| first_name | query | First name for the user. | No |  |
| last_name | query | Last name for the user. | No |  |
| phone | query | Phone number for the user. | No |  |
| email | query | The email address for the user. | No |  |
| nickname | query | The nickname for the user. | No |  |
| password | query | Password for the user (never included). | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /vendor-staff/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | query | Login name for the user. | No |  |
| name | query | Display name for the user. | No |  |
| first_name | query | First name for the user. | No |  |
| last_name | query | Last name for the user. | No |  |
| phone | query | Phone number for the user. | No |  |
| email | query | The email address for the user. | No |  |
| nickname | query | The nickname for the user. | No |  |
| password | query | Password for the user (never included). | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /vendor-staff/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | query | Login name for the user. | No |  |
| name | query | Display name for the user. | No |  |
| first_name | query | First name for the user. | No |  |
| last_name | query | Last name for the user. | No |  |
| phone | query | Phone number for the user. | No |  |
| email | query | The email address for the user. | No |  |
| nickname | query | The nickname for the user. | No |  |
| password | query | Password for the user (never included). | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /vendor-staff/{id}` 

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

# /VENDOR-STAFF/{ID}/CAPABILITIES
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-staff/{id}/capabilities` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /vendor-staff/{id}/capabilities` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| capabilities | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /vendor-staff/{id}/capabilities` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| capabilities | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /vendor-staff/{id}/capabilities` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| capabilities | query |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VENDOR-STAFF/CAPABILITIES
## ***GET*** 

### HTTP Request 
`***GET*** /vendor-staff/capabilities` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /WHOLESALE/REGISTER
## ***POST*** 

### HTTP Request 
`***POST*** /wholesale/register` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query | User ID. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /WHOLESALE/CUSTOMERS
## ***GET*** 

### HTTP Request 
`***GET*** /wholesale/customers` 

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

# /WHOLESALE/CUSTOMER/{ID}
## ***POST*** 

### HTTP Request 
`***POST*** /wholesale/customer/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Status for wholesale customer | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /wholesale/customer/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Status for wholesale customer | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /wholesale/customer/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | Unique identifier for the object. | Yes |  |
| status | query | Status for wholesale customer | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /WHOLESALE/CUSTOMERS/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /wholesale/customers/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /wholesale/customers/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /wholesale/customers/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REQUEST-FOR-QUOTE
## ***GET*** 

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

## ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REQUEST-FOR-QUOTE/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /REQUEST-FOR-QUOTE/{ID}/RESTORE
## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /REQUEST-FOR-QUOTE/BATCH
## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /REQUEST-FOR-QUOTE/CONVERT-TO-ORDER
## ***POST*** 

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

# /REQUEST-FOR-QUOTE/QUOTE-RULE
## ***GET*** 

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

## ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/quote-rule` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REQUEST-FOR-QUOTE/QUOTE-RULE/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /REQUEST-FOR-QUOTE/QUOTE-RULE/BATCH
## ***POST*** 

### HTTP Request 
`***POST*** /request-for-quote/quote-rule/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /request-for-quote/quote-rule/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /request-for-quote/quote-rule/batch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /REQUEST-FOR-QUOTE/QUOTE-RULE/{ID}/RESTORE
## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /REQUEST-FOR-QUOTE/CUSTOMERS
## ***GET*** 

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

## ***POST*** 

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

# /REQUEST-FOR-QUOTE/CUSTOMERS/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /REQUEST-FOR-QUOTE/CUSTOMERS/BATCH
## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

# /REQUEST-FOR-QUOTE/ROLES
## ***GET*** 

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

# /VERIFICATION-METHODS
## ***GET*** 

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

## ***POST*** 

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

# /VERIFICATION-METHODS/{ID}
## ***GET*** 

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

## ***POST*** 

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

## ***PUT*** 

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

## ***PATCH*** 

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

## ***DELETE*** 

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

# /VERIFICATION-REQUESTS
## ***GET*** 

### HTTP Request 
`***GET*** /verification-requests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| vendor_id | query | Vendor ID associated with the verification request. | No |  |
| method_id | query | Verification Method ID associated with the verification request. | No |  |
| status | query | The document type is enabled or not | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***POST*** 

### HTTP Request 
`***POST*** /verification-requests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | Yes |  |
| method_id | query | Verification Method id associated with verification request. | Yes |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

# /VERIFICATION-REQUESTS/{ID}
## ***GET*** 

### HTTP Request 
`***GET*** /verification-requests/{id}` 

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

## ***POST*** 

### HTTP Request 
`***POST*** /verification-requests/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | No |  |
| method_id | query | Verification Method id associated with verification request. | No |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PUT*** 

### HTTP Request 
`***PUT*** /verification-requests/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | No |  |
| method_id | query | Verification Method id associated with verification request. | No |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***PATCH*** 

### HTTP Request 
`***PATCH*** /verification-requests/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | No |  |
| method_id | query | Verification Method id associated with verification request. | No |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## ***DELETE*** 

### HTTP Request 
`***DELETE*** /verification-requests/{id}` 

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
