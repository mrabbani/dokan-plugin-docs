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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
