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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
