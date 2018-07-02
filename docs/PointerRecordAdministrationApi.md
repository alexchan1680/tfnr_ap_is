# TfnrApIs.PointerRecordAdministrationApi

All URIs are relative to *https://api-devp-tfnregistry.somos.com/v1/ip*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pointerRecordCopy**](PointerRecordAdministrationApi.md#pointerRecordCopy) | **POST** /cus/pointer/copy | Pointer Record Copy
[**pointerRecordCopyByRequestId**](PointerRecordAdministrationApi.md#pointerRecordCopyByRequestId) | **GET** /cus/pointer/copy/{requestId} | Pointer Record Copy - Sync Timeout
[**pointerRecordCopyUdateByRequestId**](PointerRecordAdministrationApi.md#pointerRecordCopyUdateByRequestId) | **GET** /cus/pointer/copyUpdate/{requestId} | Pointer Record Copy Update - Sync Timeout
[**pointerRecordCopyUpdate**](PointerRecordAdministrationApi.md#pointerRecordCopyUpdate) | **PUT** /cus/pointer/copyUpdate | Pointer Record Copy Update
[**pointerRecordCreate**](PointerRecordAdministrationApi.md#pointerRecordCreate) | **POST** /cus/pointer/create | Pointer Record Create
[**pointerRecordCreateByRequestId**](PointerRecordAdministrationApi.md#pointerRecordCreateByRequestId) | **GET** /cus/pointer/create/{requestId} | Pointer Record Create - Sync Timeout
[**pointerRecordDelete**](PointerRecordAdministrationApi.md#pointerRecordDelete) | **POST** /cus/pointer/delete | Pointer Record Delete
[**pointerRecordDeleteByRequestId**](PointerRecordAdministrationApi.md#pointerRecordDeleteByRequestId) | **GET** /cus/pointer/delete/{requestId} | Pointer Record Delete - Sync Timeout
[**pointerRecordDisconnect**](PointerRecordAdministrationApi.md#pointerRecordDisconnect) | **PUT** /cus/pointer/disconnect | Pointer Record Disconnect
[**pointerRecordDisconnectByRequestId**](PointerRecordAdministrationApi.md#pointerRecordDisconnectByRequestId) | **GET** /cus/pointer/disconnect/{requestId} | Pointer Record Disconnect - Sync Timeout
[**pointerRecordDisconnectUpdate**](PointerRecordAdministrationApi.md#pointerRecordDisconnectUpdate) | **PUT** /cus/pointer/disconnectUpdate | Pointer Record Disconnect Update
[**pointerRecordDisconnectUpdateByRequestId**](PointerRecordAdministrationApi.md#pointerRecordDisconnectUpdateByRequestId) | **GET** /cus/pointer/disconnectUpdate/{requestId} | Pointer Record Disconnect Update - Sync Timeout
[**pointerRecordTransfer**](PointerRecordAdministrationApi.md#pointerRecordTransfer) | **PUT** /cus/pointer/transfer | Pointer Record Transfer
[**pointerRecordTransferByRequestId**](PointerRecordAdministrationApi.md#pointerRecordTransferByRequestId) | **GET** /cus/pointer/transfer/{requestId} | Pointer Record Transfer - Sync Timeout
[**pointerRecordTransferUpdate**](PointerRecordAdministrationApi.md#pointerRecordTransferUpdate) | **PUT** /cus/pointer/transferUpdate | Pointer Record Transfer Update
[**pointerRecordTransferUpdateByRequestId**](PointerRecordAdministrationApi.md#pointerRecordTransferUpdateByRequestId) | **GET** /cus/pointer/transferUpdate/{requestId} | Pointer Record Transfer Update - Sync Timeout
[**pointerRecordUpdate**](PointerRecordAdministrationApi.md#pointerRecordUpdate) | **PUT** /cus/pointer/update | Pointer Record Update
[**pointerRecordUpdateByRequestId**](PointerRecordAdministrationApi.md#pointerRecordUpdateByRequestId) | **GET** /cus/pointer/update/{requestId} | Pointer Record Update - Sync Timeout
[**pointerRecordView**](PointerRecordAdministrationApi.md#pointerRecordView) | **GET** /cus/pointer/view | Pointer Record View
[**pointerRecordViewByRequestId**](PointerRecordAdministrationApi.md#pointerRecordViewByRequestId) | **GET** /cus/pointer/view/{requestId} | Pointer Record View - Sync Timeout


<a name="pointerRecordCopy"></a>
# **pointerRecordCopy**
> PointerCopyResponse pointerRecordCopy(authorization, body)

Pointer Record Copy

The request is meant to allow for a copy a pointer record to allow for a future effective data or now or a different section (such as CAD/LAD/CPR).Note that the flags for whether or not to copy specific areas will be applied to only copy what is requested. The flags will determine if the sections of data they are associated with will be copied. Also note, if tgtNum(target) is different than the num(Source),then tgtNum should be in working or assigned status.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.PointerCopyRequest(); // PointerCopyRequest | 


apiInstance.pointerRecordCopy(authorization, body, (error, data, response) => {
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
 **body** | [**PointerCopyRequest**](PointerCopyRequest.md)|  | 

### Return type

[**PointerCopyResponse**](PointerCopyResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordCopyByRequestId"></a>
# **pointerRecordCopyByRequestId**
> PointerCopyResponse pointerRecordCopyByRequestId(authorization, requestId)

Pointer Record Copy - Sync Timeout

This API is used if /cus/record/copy api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordCopyByRequestId(authorization, requestId, (error, data, response) => {
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

[**PointerCopyResponse**](PointerCopyResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordCopyUdateByRequestId"></a>
# **pointerRecordCopyUdateByRequestId**
> PointerCopyUpdateResponse pointerRecordCopyUdateByRequestId(authorization, requestId)

Pointer Record Copy Update - Sync Timeout

This API is used if /cus/pointer/copyUpdate API returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordCopyUdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**PointerCopyUpdateResponse**](PointerCopyUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordCopyUpdate"></a>
# **pointerRecordCopyUpdate**
> PointerCopyUpdateResponse pointerRecordCopyUpdate(authorization, body)

Pointer Record Copy Update

This API is used to update a record to complete the copy. Before calling this API, it is Recommended to invoke /cus/pointer/copy, and create a copy record. This API has anyOf parameters: suppFormNum or svcOrderNum.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.PointerCopyUpdateRequest(); // PointerCopyUpdateRequest | 


apiInstance.pointerRecordCopyUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**PointerCopyUpdateRequest**](PointerCopyUpdateRequest.md)|  | 

### Return type

[**PointerCopyUpdateResponse**](PointerCopyUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordCreate"></a>
# **pointerRecordCreate**
> PointerCreateResponse pointerRecordCreate(authorization, body)

Pointer Record Create

This API is used to create a pointer record. This API has anyOf parameters: suppFormNum or svcOrderNum.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.PointerCreateRequest(); // PointerCreateRequest | 


apiInstance.pointerRecordCreate(authorization, body, (error, data, response) => {
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
 **body** | [**PointerCreateRequest**](PointerCreateRequest.md)|  | 

### Return type

[**PointerCreateResponse**](PointerCreateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordCreateByRequestId"></a>
# **pointerRecordCreateByRequestId**
> PointerCreateResponse pointerRecordCreateByRequestId(authorization, requestId)

Pointer Record Create - Sync Timeout

This API is used if /cus/pointer/create api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordCreateByRequestId(authorization, requestId, (error, data, response) => {
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

[**PointerCreateResponse**](PointerCreateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordDelete"></a>
# **pointerRecordDelete**
> DeletePointerResponse pointerRecordDelete(authorization, body)

Pointer Record Delete

This API will allow the user to delete an existing Customer Pointer Record for the provided effective date and time.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.DeletePointerRequest(); // DeletePointerRequest | 


apiInstance.pointerRecordDelete(authorization, body, (error, data, response) => {
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
 **body** | [**DeletePointerRequest**](DeletePointerRequest.md)|  | 

### Return type

[**DeletePointerResponse**](DeletePointerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordDeleteByRequestId"></a>
# **pointerRecordDeleteByRequestId**
> DeletePointerResponse pointerRecordDeleteByRequestId(authorization, requestId)

Pointer Record Delete - Sync Timeout

This API is used if /cus/pointer/delete API returns a HTTP 202 with a RequestID in the pay load. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordDeleteByRequestId(authorization, requestId, (error, data, response) => {
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

[**DeletePointerResponse**](DeletePointerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordDisconnect"></a>
# **pointerRecordDisconnect**
> DisconnectPointerResponse pointerRecordDisconnect(authorization, body)

Pointer Record Disconnect

This API is used to create a Disconnect Pointer Record for the effective date, and time. This API has anyOf parameters: suppFormNum or svcOrderNum.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.DisconnectPointerRequest(); // DisconnectPointerRequest | 


apiInstance.pointerRecordDisconnect(authorization, body, (error, data, response) => {
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
 **body** | [**DisconnectPointerRequest**](DisconnectPointerRequest.md)|  | 

### Return type

[**DisconnectPointerResponse**](DisconnectPointerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordDisconnectByRequestId"></a>
# **pointerRecordDisconnectByRequestId**
> DisconnectPointerResponse pointerRecordDisconnectByRequestId(authorization, requestId)

Pointer Record Disconnect - Sync Timeout

This API is used if /cus/pointer/disconnect api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordDisconnectByRequestId(authorization, requestId, (error, data, response) => {
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

[**DisconnectPointerResponse**](DisconnectPointerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordDisconnectUpdate"></a>
# **pointerRecordDisconnectUpdate**
> DisconnectUpdatePointerResponse pointerRecordDisconnectUpdate(authorization, body)

Pointer Record Disconnect Update

This API is used to update the Disconnect Pointer Record. This API has anyOf parameters: suppFormNum or svcOrderNum.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.DisconnectUpdatePointerRequest(); // DisconnectUpdatePointerRequest | 


apiInstance.pointerRecordDisconnectUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**DisconnectUpdatePointerRequest**](DisconnectUpdatePointerRequest.md)|  | 

### Return type

[**DisconnectUpdatePointerResponse**](DisconnectUpdatePointerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordDisconnectUpdateByRequestId"></a>
# **pointerRecordDisconnectUpdateByRequestId**
> DisconnectUpdatePointerResponse pointerRecordDisconnectUpdateByRequestId(authorization, requestId)

Pointer Record Disconnect Update - Sync Timeout

This API is used if /cus/pointer/disconnectUpdate api returns a HTTP 202 with a RequestID in the pay load. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordDisconnectUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**DisconnectUpdatePointerResponse**](DisconnectUpdatePointerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordTransfer"></a>
# **pointerRecordTransfer**
> PointerTransferResponse pointerRecordTransfer(authorization, body)

Pointer Record Transfer

This API is used to transfer a customer pointer record to a future effective date.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.PointerTransferRequest(); // PointerTransferRequest | 


apiInstance.pointerRecordTransfer(authorization, body, (error, data, response) => {
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
 **body** | [**PointerTransferRequest**](PointerTransferRequest.md)|  | 

### Return type

[**PointerTransferResponse**](PointerTransferResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordTransferByRequestId"></a>
# **pointerRecordTransferByRequestId**
> PointerTransferResponse pointerRecordTransferByRequestId(authorization, requestId)

Pointer Record Transfer - Sync Timeout

This API is used if /cus/pointer/transfer API returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordTransferByRequestId(authorization, requestId, (error, data, response) => {
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

[**PointerTransferResponse**](PointerTransferResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordTransferUpdate"></a>
# **pointerRecordTransferUpdate**
> PointerTransferUpdateResponse pointerRecordTransferUpdate(authorization, body)

Pointer Record Transfer Update

This API is used to update a record to complete the transfer. The Transfer update will allow for the change on the record post the transfer command. Before calling this API it is REQUIRED to invoke /cus/pointer/transfer, and create a transfer record. This API has anyOf parameters: suppFormNum or svcOrderNum.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.PointerTransferUpdateRequest(); // PointerTransferUpdateRequest | 


apiInstance.pointerRecordTransferUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**PointerTransferUpdateRequest**](PointerTransferUpdateRequest.md)|  | 

### Return type

[**PointerTransferUpdateResponse**](PointerTransferUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordTransferUpdateByRequestId"></a>
# **pointerRecordTransferUpdateByRequestId**
> PointerTransferUpdateResponse pointerRecordTransferUpdateByRequestId(authorization, requestId)

Pointer Record Transfer Update - Sync Timeout

This API is used if /cus/pointer/transferUpdate API returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordTransferUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**PointerTransferUpdateResponse**](PointerTransferUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordUpdate"></a>
# **pointerRecordUpdate**
> PointerUpdateResponse pointerRecordUpdate(authorization, body)

Pointer Record Update

This API is used to update a Pointer Record for a dial number. This API has anyOf parameters: suppFormNum or svcOrderNum.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.PointerUpdateRequest(); // PointerUpdateRequest | 


apiInstance.pointerRecordUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**PointerUpdateRequest**](PointerUpdateRequest.md)|  | 

### Return type

[**PointerUpdateResponse**](PointerUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordUpdateByRequestId"></a>
# **pointerRecordUpdateByRequestId**
> PointerUpdateResponse pointerRecordUpdateByRequestId(authorization, requestId)

Pointer Record Update - Sync Timeout

This API is used if /cus/pointer/update api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**PointerUpdateResponse**](PointerUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordView"></a>
# **pointerRecordView**
> PointerRetrieveResponse pointerRecordView(authorization, num, opts)

Pointer Record View

This API is used to retrieve a list of possible records based on the provided dialed number, and effective date time.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let num = "num_example"; // String | dialed Number

let opts = { 
  'effDtTm': "effDtTm_example" // String | Effective date and time
};

apiInstance.pointerRecordView(authorization, num, opts, (error, data, response) => {
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
 **num** | **String**| dialed Number | 
 **effDtTm** | **String**| Effective date and time | [optional] 

### Return type

[**PointerRetrieveResponse**](PointerRetrieveResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="pointerRecordViewByRequestId"></a>
# **pointerRecordViewByRequestId**
> PointerRetrieveResponse pointerRecordViewByRequestId(authorization, requestId)

Pointer Record View - Sync Timeout

This API is used if /cus/pointer/view api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PointerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.pointerRecordViewByRequestId(authorization, requestId, (error, data, response) => {
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

[**PointerRetrieveResponse**](PointerRetrieveResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

