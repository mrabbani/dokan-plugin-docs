# VERIFICATION-REQUESTS
### ***GET*** 

### HTTP Request 
`***GET*** /verification-requests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| context | query | Scope under which the request is made; determines fields present in response. | No |  |
| page | query | Current page of the collection. | No |  |
| per_page | query | Maximum number of items to be returned in result set. | No |  |
| vendor_id | query | Vendor ID associated with the verification request. | No |  |
| method_id | query | Verification Method ID associated with the verification request. | No |  |
| status | query | The document type is enabled or not | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***POST*** 

### HTTP Request 
`***POST*** /verification-requests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | Yes |  |
| method_id | query | Verification Method id associated with verification request. | Yes |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

## /VERIFICATION-REQUESTS/{ID}
### ***GET*** 

### HTTP Request 
`***GET*** /verification-requests/{id}` 

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

### ***POST*** 

### HTTP Request 
`***POST*** /verification-requests/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | No |  |
| method_id | query | Verification Method id associated with verification request. | No |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PUT*** 

### HTTP Request 
`***PUT*** /verification-requests/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | No |  |
| method_id | query | Verification Method id associated with verification request. | No |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***PATCH*** 

### HTTP Request 
`***PATCH*** /verification-requests/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | query | Vendor id associated with verification request. | No |  |
| method_id | query | Verification Method id associated with verification request. | No |  |
| status | query | The verification request status. | No |  |
| note | query | The verification request note for administrator. | No |  |
| additional_info | query | The documents additional information. | No |  |
| documents | query | The documents for verification | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 404 | Not Found |

### ***DELETE*** 

### HTTP Request 
`***DELETE*** /verification-requests/{id}` 

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

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
