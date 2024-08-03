# PRODUCTS
### ***GET*** 

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

### ***POST*** 

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

## /PRODUCTS/{ID}
### ***GET*** 

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

### ***POST*** 

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

### ***PUT*** 

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

### ***PATCH*** 

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

### ***DELETE*** 

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

## /PRODUCTS/SUMMARY
### ***GET*** 

### HTTP Request 
`***GET*** /products/summary` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /PRODUCTS/{ID}/RELATED
### ***GET*** 

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

## /PRODUCTS/TOP_RATED
### ***GET*** 

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

## /PRODUCTS/BEST_SELLING
### ***GET*** 

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

## /PRODUCTS/FEATURED
### ***GET*** 

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

## /PRODUCTS/LATEST
### ***GET*** 

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

## /PRODUCTS/MULTISTEP-CATEGORIES
### ***GET*** 

### HTTP Request 
`***GET*** /products/multistep-categories` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /PRODUCTS/ATTRIBUTES
### ***GET*** 

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

### ***POST*** 

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

## /PRODUCTS/ATTRIBUTES/{ID}
### ***GET*** 

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

### ***POST*** 

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

### ***PUT*** 

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

### ***PATCH*** 

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

### ***DELETE*** 

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

## /PRODUCTS/ATTRIBUTES/BATCH
### ***POST*** 

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

### ***PUT*** 

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

### ***PATCH*** 

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

## /PRODUCTS/ATTRIBUTES/EDIT-PRODUCT/{ID}
### ***POST*** 

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

### ***PUT*** 

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

### ***PATCH*** 

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

## /PRODUCTS/ATTRIBUTES/SET-DEFAULT/{ID}
### ***POST*** 

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

### ***PUT*** 

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

### ***PATCH*** 

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

## /PRODUCTS/ATTRIBUTES/{ATTRIBUTE_ID}/TERMS
### ***GET*** 

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

### ***POST*** 

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

## /PRODUCTS/ATTRIBUTES/{ATTRIBUTE_ID}/TERMS/{ID}
### ***GET*** 

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

### ***POST*** 

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

### ***PUT*** 

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

### ***PATCH*** 

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

### ***DELETE*** 

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

## /PRODUCTS/ATTRIBUTES/{ATTRIBUTE_ID}/TERMS/BATCH
### ***POST*** 

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

### ***PUT*** 

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

### ***PATCH*** 

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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
