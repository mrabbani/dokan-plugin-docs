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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
