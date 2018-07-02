# TfnrApIs.BulkAdministration_Api

All URIs are relative to *https://api-devp-tfnregistry.somos.com/v1/ip*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulkCount**](BulkAdministration_Api.md#bulkCount) | **GET** /sys/bulk/count | Bulk Count 
[**bulkCountbyRequestId**](BulkAdministration_Api.md#bulkCountbyRequestId) | **GET** /sys/bulk/count/{requestId} | Bulk Count - Sync Timeout 
[**bulkDelete**](BulkAdministration_Api.md#bulkDelete) | **PUT** /sys/bulk/delete | Bulk Delete 
[**bulkDeletebyRequestId**](BulkAdministration_Api.md#bulkDeletebyRequestId) | **GET** /sys/bulk/delete/{requestId} | Bulk Delete - Sync Timeout 
[**bulkList**](BulkAdministration_Api.md#bulkList) | **GET** /sys/bulk/list | Bulk List 
[**bulkListSyncTimeout**](BulkAdministration_Api.md#bulkListSyncTimeout) | **GET** /sys/bulk/list/{requestId} | Bulk List - Sync Timeout 


<a name="bulkCount"></a>
# **bulkCount**
> CountBulkResponse bulkCount(authorization)

Bulk Count 

This API is used to get the count of Bulk Requests created by providing the Resp Org ID in the request. User receives response with count value. The count value represents the number of Bulk Requests that are not pending or queued and not yet retrieved at least once.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.BulkAdministration_Api();

let authorization = "authorization_example"; // String | Bearer access_token


apiInstance.bulkCount(authorization, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **String**| Bearer access_token | 

### Return type

[**CountBulkResponse**](CountBulkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="bulkCountbyRequestId"></a>
# **bulkCountbyRequestId**
> CountBulkResponse bulkCountbyRequestId(authorization, requestId)

Bulk Count - Sync Timeout 

This API is used to get the count of Bulk Requests created by providing the Resp Org ID in the request. User receives response with count value. The count value represents the number of Bulk Requests that are not pending or queued and not yet retrieved at least once.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.BulkAdministration_Api();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.bulkCountbyRequestId(authorization, requestId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **String**| Bearer access_token | 
 **requestId** | **Number**| RequestId returned due to timeout | 

### Return type

[**CountBulkResponse**](CountBulkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="bulkDelete"></a>
# **bulkDelete**
> DeleteBulkResponse bulkDelete(authorization, body)

Bulk Delete 

This API is used to delete (soft delete) a record of the bulk search result.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.BulkAdministration_Api();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.DeleteBulkRequest(); // DeleteBulkRequest | 


apiInstance.bulkDelete(authorization, body, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **String**| Bearer access_token | 
 **body** | [**DeleteBulkRequest**](DeleteBulkRequest.md)|  | 

### Return type

[**DeleteBulkResponse**](DeleteBulkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="bulkDeletebyRequestId"></a>
# **bulkDeletebyRequestId**
> DeleteBulkResponse bulkDeletebyRequestId(authorization, requestId)

Bulk Delete - Sync Timeout 

This API is used to delete (soft delete) a record of the bulk search result.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.BulkAdministration_Api();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.bulkDeletebyRequestId(authorization, requestId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **String**| Bearer access_token | 
 **requestId** | **Number**| RequestId returned due to timeout | 

### Return type

[**DeleteBulkResponse**](DeleteBulkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="bulkList"></a>
# **bulkList**
> ListBulkResponse bulkList(authorization)

Bulk List 

This API lists the status of bulk search results. It pulls all the active records.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.BulkAdministration_Api();

let authorization = "authorization_example"; // String | Bearer access_token


apiInstance.bulkList(authorization, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **String**| Bearer access_token | 

### Return type

[**ListBulkResponse**](ListBulkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="bulkListSyncTimeout"></a>
# **bulkListSyncTimeout**
> ListBulkResponse bulkListSyncTimeout(authorization, requestId)

Bulk List - Sync Timeout 

This API lists the status of bulk search results. It pulls all the active records.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.BulkAdministration_Api();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.bulkListSyncTimeout(authorization, requestId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **String**| Bearer access_token | 
 **requestId** | **Number**| RequestId returned due to timeout | 

### Return type

[**ListBulkResponse**](ListBulkResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

