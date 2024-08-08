# SPMV-PRODUCT/SETTINGS
## /SPMV-PRODUCT/SETTINGS
### ***GET*** 

### HTTP Request 
`***GET*** /spmv-product/settings` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /SPMV-PRODUCT/SEARCH
### ***GET*** 

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

## /SPMV-PRODUCT/ADD-TO-STORE
### ***POST*** 

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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
