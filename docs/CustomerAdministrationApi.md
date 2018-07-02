# TfnrApIs.CustomerAdministrationApi

All URIs are relative to *https://api-devp-tfnregistry.somos.com/v1/ip*

Method | HTTP request | Description
------------- | ------------- | -------------
[**customerUnlock**](CustomerAdministrationApi.md#customerUnlock) | **PUT** /cus/unlock | Customer Unlock
[**customerUnlockByRequestId**](CustomerAdministrationApi.md#customerUnlockByRequestId) | **GET** /cus/unlock/{requestId} | Customer Unlock - Sync Timeout


<a name="customerUnlock"></a>
# **customerUnlock**
> CustomerUnlockResponse customerUnlock(authorization, body)

Customer Unlock

This API is used to release the lock which was applied during customer record retrieval time. It allows another user to retrieve that record.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.CustomerUnlockRequest(); // CustomerUnlockRequest | 


apiInstance.customerUnlock(authorization, body, (error, data, response) => {
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
 **body** | [**CustomerUnlockRequest**](CustomerUnlockRequest.md)|  | 

### Return type

[**CustomerUnlockResponse**](CustomerUnlockResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerUnlockByRequestId"></a>
# **customerUnlockByRequestId**
> CustomerUnlockResponse customerUnlockByRequestId(authorization, requestId)

Customer Unlock - Sync Timeout

This API is used to release the lock which was applied during customer record retrieval time. It allows another user to retrieve that record.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerUnlockByRequestId(authorization, requestId, (error, data, response) => {
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

[**CustomerUnlockResponse**](CustomerUnlockResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

