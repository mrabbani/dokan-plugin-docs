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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
