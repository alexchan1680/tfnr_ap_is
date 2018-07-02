# TfnrApIs.CustomerRecordAdministrationApi

All URIs are relative to *https://api-devp-tfnregistry.somos.com/v1/ip*

Method | HTTP request | Description
------------- | ------------- | -------------
[**customerRecordCopy**](CustomerRecordAdministrationApi.md#customerRecordCopy) | **POST** /cus/record/copy | Customer Record Copy
[**customerRecordCopyByRequestId**](CustomerRecordAdministrationApi.md#customerRecordCopyByRequestId) | **GET** /cus/record/copy/{requestId} | Customer Record Copy - Sync Timeout
[**customerRecordCopyUpdate**](CustomerRecordAdministrationApi.md#customerRecordCopyUpdate) | **PUT** /cus/record/copyUpdate | Customer Record Copy Update
[**customerRecordCopyUpdateByRequestId**](CustomerRecordAdministrationApi.md#customerRecordCopyUpdateByRequestId) | **GET** /cus/record/copyUpdate/{requestId} | Customer Record Copy Update - Sync Timeout
[**customerRecordCreate**](CustomerRecordAdministrationApi.md#customerRecordCreate) | **POST** /cus/record/create | Customer Record Create 
[**customerRecordCreateByRequestId**](CustomerRecordAdministrationApi.md#customerRecordCreateByRequestId) | **GET** /cus/record/create/{requestId} | Customer Record Create - Sync Timeout
[**customerRecordDelete**](CustomerRecordAdministrationApi.md#customerRecordDelete) | **POST** /cus/record/delete | Customer Record Delete
[**customerRecordDeleteByRequestId**](CustomerRecordAdministrationApi.md#customerRecordDeleteByRequestId) | **GET** /cus/record/delete/{requestId} | Customer Record Delete - Sync Timeout
[**customerRecordDisconnect**](CustomerRecordAdministrationApi.md#customerRecordDisconnect) | **PUT** /cus/record/disconnect | Customer Record Disconnect
[**customerRecordDisconnectByRequestId**](CustomerRecordAdministrationApi.md#customerRecordDisconnectByRequestId) | **GET** /cus/record/disconnect/{requestId} | Customer Record Disconnect - Sync Timeout
[**customerRecordDisconnectUpdate**](CustomerRecordAdministrationApi.md#customerRecordDisconnectUpdate) | **PUT** /cus/record/disconnectUpdate | Customer Record Disconnect Update
[**customerRecordDisconnectUpdateByRequestId**](CustomerRecordAdministrationApi.md#customerRecordDisconnectUpdateByRequestId) | **GET** /cus/record/disconnectUpdate/{requestId} | Customer Record Disconnect Update - Sync Timeout
[**customerRecordQuery**](CustomerRecordAdministrationApi.md#customerRecordQuery) | **GET** /cus/record/query | Customer Record Query
[**customerRecordTransfer**](CustomerRecordAdministrationApi.md#customerRecordTransfer) | **PUT** /cus/record/transfer | Customer Record Transfer
[**customerRecordTransferByRequestId**](CustomerRecordAdministrationApi.md#customerRecordTransferByRequestId) | **GET** /cus/record/transfer/{requestId} | Customer Record Transfer - Sync Timeout
[**customerRecordTransferUpdate**](CustomerRecordAdministrationApi.md#customerRecordTransferUpdate) | **PUT** /cus/record/transferUpdate | Customer Record Transfer Update
[**customerRecordTransferUpdateByRequestId**](CustomerRecordAdministrationApi.md#customerRecordTransferUpdateByRequestId) | **GET** /cus/record/transferUpdate/{requestId} | Customer Record Transfer Update - Sync Timeout
[**customerRecordUpdate**](CustomerRecordAdministrationApi.md#customerRecordUpdate) | **PUT** /cus/record/update | Customer Record Update
[**customerRecordUpdateByRequestId**](CustomerRecordAdministrationApi.md#customerRecordUpdateByRequestId) | **GET** /cus/record/update/{requestId} | Customer Record Update - Sync Timeout
[**customerRecordView**](CustomerRecordAdministrationApi.md#customerRecordView) | **GET** /cus/record/view | Customer Record View
[**customerRecordViewByRequestId**](CustomerRecordAdministrationApi.md#customerRecordViewByRequestId) | **GET** /cus/record/view/{requestId} | Customer Record View - Sync Timeout


<a name="customerRecordCopy"></a>
# **customerRecordCopy**
> RecordCopyResponse customerRecordCopy(authorization, body)

Customer Record Copy

The request is meant to allow for a copy a customer record to allow for a future effective data or now or different sections(such as CAD/LAD/CPR) to another dial number. Note that the flags for whether or not to copy specific areas will be applied to only copy what is requested. The flags will determine if the sections of data they are associated with will be copied. Also note, if tgtNum(target) is different than the num(Source),then tgtNum should be in working or assigned status.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordCopyRequest(); // RecordCopyRequest | 


apiInstance.customerRecordCopy(authorization, body, (error, data, response) => {
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
 **body** | [**RecordCopyRequest**](RecordCopyRequest.md)|  | 

### Return type

[**RecordCopyResponse**](RecordCopyResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordCopyByRequestId"></a>
# **customerRecordCopyByRequestId**
> RecordCopyResponse customerRecordCopyByRequestId(authorization, requestId)

Customer Record Copy - Sync Timeout

This API is used if /cus/record/copy api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordCopyByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordCopyResponse**](RecordCopyResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordCopyUpdate"></a>
# **customerRecordCopyUpdate**
> RecordCopyUpdateResponse customerRecordCopyUpdate(authorization, body)

Customer Record Copy Update

This API is used to complete the copy, by updating the record. Before calling this API, it is recommended to invoke /cus/record/copy, and create a copy record. This API has anyOf parameters: suppFormNum or svcOrderNum and interLTCar or intraLTCar.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordCopyUpdateRequest(); // RecordCopyUpdateRequest | 


apiInstance.customerRecordCopyUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**RecordCopyUpdateRequest**](RecordCopyUpdateRequest.md)|  | 

### Return type

[**RecordCopyUpdateResponse**](RecordCopyUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordCopyUpdateByRequestId"></a>
# **customerRecordCopyUpdateByRequestId**
> RecordCopyUpdateResponse customerRecordCopyUpdateByRequestId(authorization, requestId)

Customer Record Copy Update - Sync Timeout

This API is used if /cus/record/copyUpdate api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordCopyUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordCopyUpdateResponse**](RecordCopyUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordCreate"></a>
# **customerRecordCreate**
> RecordCreateResponse customerRecordCreate(authorization, body)

Customer Record Create 

This API is used to create a customer record. This API has anyOf parameters: suppFormNum or svcOrderNum and interLTCar or intraLTCar. This API should not be used for activating a number in DISCONNECT status, instead use /cus/record/copyUpdate.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordCreateRequest(); // RecordCreateRequest | 


apiInstance.customerRecordCreate(authorization, body, (error, data, response) => {
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
 **body** | [**RecordCreateRequest**](RecordCreateRequest.md)|  | 

### Return type

[**RecordCreateResponse**](RecordCreateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordCreateByRequestId"></a>
# **customerRecordCreateByRequestId**
> RecordCreateResponse customerRecordCreateByRequestId(authorization, requestId)

Customer Record Create - Sync Timeout

This API is used if /cus/record/create api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordCreateByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordCreateResponse**](RecordCreateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordDelete"></a>
# **customerRecordDelete**
> RecordDeleteResponse customerRecordDelete(authorization, body)

Customer Record Delete

This API will allow the user to delete an existing Customer Record for the provided effective date and time.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordDeleteRequest(); // RecordDeleteRequest | 


apiInstance.customerRecordDelete(authorization, body, (error, data, response) => {
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
 **body** | [**RecordDeleteRequest**](RecordDeleteRequest.md)|  | 

### Return type

[**RecordDeleteResponse**](RecordDeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordDeleteByRequestId"></a>
# **customerRecordDeleteByRequestId**
> RecordDeleteResponse customerRecordDeleteByRequestId(authorization, requestId)

Customer Record Delete - Sync Timeout

This API is used if /cus/record/delete api returns a HTTP 202 with a RequestID in the pay load. Please see the section Polling for more information on how to do the polling. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordDeleteByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordDeleteResponse**](RecordDeleteResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordDisconnect"></a>
# **customerRecordDisconnect**
> DisconnectCustomerResponse customerRecordDisconnect(authorization, body)

Customer Record Disconnect

This API is used to create a Disconnect Record for the effective date and time. This API has anyOf parameters: suppFormNum or svcOrderNum and interLTCar or intraLTCar.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.DisconnectCustomerRequest(); // DisconnectCustomerRequest | 


apiInstance.customerRecordDisconnect(authorization, body, (error, data, response) => {
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
 **body** | [**DisconnectCustomerRequest**](DisconnectCustomerRequest.md)|  | 

### Return type

[**DisconnectCustomerResponse**](DisconnectCustomerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordDisconnectByRequestId"></a>
# **customerRecordDisconnectByRequestId**
> DisconnectCustomerResponse customerRecordDisconnectByRequestId(authorization, requestId)

Customer Record Disconnect - Sync Timeout

This API is used if /cus/record/disconnect api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordDisconnectByRequestId(authorization, requestId, (error, data, response) => {
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

[**DisconnectCustomerResponse**](DisconnectCustomerResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordDisconnectUpdate"></a>
# **customerRecordDisconnectUpdate**
> RecordDisconnectUpdateResponse customerRecordDisconnectUpdate(authorization, body)

Customer Record Disconnect Update

This API is used to update the Disconnect Record. This API has anyOf parameters: suppFormNum or svcOrderNum and interLTCar or intraLTCar.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordDisconnectUpdateRequest(); // RecordDisconnectUpdateRequest | 


apiInstance.customerRecordDisconnectUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**RecordDisconnectUpdateRequest**](RecordDisconnectUpdateRequest.md)|  | 

### Return type

[**RecordDisconnectUpdateResponse**](RecordDisconnectUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordDisconnectUpdateByRequestId"></a>
# **customerRecordDisconnectUpdateByRequestId**
> RecordDisconnectUpdateResponse customerRecordDisconnectUpdateByRequestId(authorization, requestId)

Customer Record Disconnect Update - Sync Timeout

This API is used if /cus/record/disconnectUpdate api returns a HTTP 202 with a RequestID in the pay load. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordDisconnectUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordDisconnectUpdateResponse**](RecordDisconnectUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordQuery"></a>
# **customerRecordQuery**
> CustomerRecordQueryResponse customerRecordQuery(authorization, num, opts)

Customer Record Query

This API provides the capability to query for the status of a Customer Record (CR). This API is used for regular (standard) customer records. There are similar APIs for Pointer records and Template records. The state of a record in the TFN Registry is reflected by one of several possible status values that are automatically generated by the system. The values are shown in the response section. If no effective date and time is requested, the API will return up to 10 versions of the customer record. The version status data will be in increasing effective date and time sequence, beginning with the earliest version. If there are more than 10 versions, an indicator will be returned informing the API client that more versions exist. If an effective date without an effective time is requested, the response message will contain status information on up to 10 versions with effective dates equal to or greater than that specified. If more than 10 versions meet the criterion, an indicator will be returned informing the API client that more versions exist.If both an effective date and an effective time are specified, the response message will return the status information on up to 10 versions with effective dates and times equal to or greater than that specified. If more than 10 versions meet the criterion, an indicator will be returned informing the API client that more versions exist. If an effective date and/or effective time are specified, and all the versions in TFN Registry have earlier effective dates and times, the API will return the most recent versions, up to a maximum of 10 versions. If there are more than 10 versions of the number, an indicator will be returned informing the API client that more versions exist

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let num = "num_example"; // String | Dialed number of the record

let opts = { 
  'effDtTime': "effDtTime_example", // String | Effective date and time format in ISO 8601
  'reqId': "reqId_example" // String | RequestId returned due to timeout
};

apiInstance.customerRecordQuery(authorization, num, opts, (error, data, response) => {
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
 **num** | **String**| Dialed number of the record | 
 **effDtTime** | **String**| Effective date and time format in ISO 8601 | [optional] 
 **reqId** | **String**| RequestId returned due to timeout | [optional] 

### Return type

[**CustomerRecordQueryResponse**](CustomerRecordQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordTransfer"></a>
# **customerRecordTransfer**
> RecordTransferResponse customerRecordTransfer(authorization, body)

Customer Record Transfer

This API is used to transfer a customer record to a future effective date.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordTransferRequest(); // RecordTransferRequest | 


apiInstance.customerRecordTransfer(authorization, body, (error, data, response) => {
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
 **body** | [**RecordTransferRequest**](RecordTransferRequest.md)|  | 

### Return type

[**RecordTransferResponse**](RecordTransferResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordTransferByRequestId"></a>
# **customerRecordTransferByRequestId**
> RecordTransferResponse customerRecordTransferByRequestId(authorization, requestId)

Customer Record Transfer - Sync Timeout

This API is used if /cus/record/transfer api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordTransferByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordTransferResponse**](RecordTransferResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordTransferUpdate"></a>
# **customerRecordTransferUpdate**
> RecordTransferUpdateResponse customerRecordTransferUpdate(authorization, body)

Customer Record Transfer Update

This API is used to update a record to complete the transfer.  The Transfer update will allow for the change on the record post the transfer command. Before calling this API it is REQUIRED to invoke /cus/record/transfer, and create a transfer record.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordTransferUpdateRequest(); // RecordTransferUpdateRequest | 


apiInstance.customerRecordTransferUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**RecordTransferUpdateRequest**](RecordTransferUpdateRequest.md)|  | 

### Return type

[**RecordTransferUpdateResponse**](RecordTransferUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordTransferUpdateByRequestId"></a>
# **customerRecordTransferUpdateByRequestId**
> RecordTransferUpdateResponse customerRecordTransferUpdateByRequestId(authorization, requestId)

Customer Record Transfer Update - Sync Timeout

This API is used if /cus/record/transferUpdate api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling. This API has anyOf parameters: suppFormNum or svcOrderNum and interLTCar or intraLTCar.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordTransferUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordTransferUpdateResponse**](RecordTransferUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordUpdate"></a>
# **customerRecordUpdate**
> RecordUpdateResponse customerRecordUpdate(authorization, body)

Customer Record Update

This API is used to update a Customer Record for a dial number. This API has anyOf parameters: suppFormNum or svcOrderNum and interLTCar or intraLTCar.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.RecordUpdateRequest(); // RecordUpdateRequest | 


apiInstance.customerRecordUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**RecordUpdateRequest**](RecordUpdateRequest.md)|  | 

### Return type

[**RecordUpdateResponse**](RecordUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordUpdateByRequestId"></a>
# **customerRecordUpdateByRequestId**
> RecordUpdateResponse customerRecordUpdateByRequestId(authorization, requestId)

Customer Record Update - Sync Timeout

This API is used if /cus/record/update api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordUpdateResponse**](RecordUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordView"></a>
# **customerRecordView**
> RecordRetrieveResponse customerRecordView(authorization, num, opts)

Customer Record View

This API is used to retrieve a list of possible records based on the number provided, and optional effective date time.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let num = "num_example"; // String | dialed Number

let opts = { 
  'effDtTm': "effDtTm_example" // String | Effective date and time
};

apiInstance.customerRecordView(authorization, num, opts, (error, data, response) => {
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

[**RecordRetrieveResponse**](RecordRetrieveResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="customerRecordViewByRequestId"></a>
# **customerRecordViewByRequestId**
> RecordRetrieveResponse customerRecordViewByRequestId(authorization, requestId)

Customer Record View - Sync Timeout

This API is used if /cus/record/view api returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.CustomerRecordAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.customerRecordViewByRequestId(authorization, requestId, (error, data, response) => {
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

[**RecordRetrieveResponse**](RecordRetrieveResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

