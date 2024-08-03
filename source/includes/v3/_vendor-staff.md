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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
