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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
