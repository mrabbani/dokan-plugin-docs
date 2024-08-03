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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
