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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
