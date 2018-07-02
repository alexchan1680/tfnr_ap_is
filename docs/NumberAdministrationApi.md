# TfnrApIs.NumberAdministrationApi

All URIs are relative to *https://api-devp-tfnregistry.somos.com/v1/ip*

Method | HTTP request | Description
------------- | ------------- | -------------
[**numberLimitsQuery**](NumberAdministrationApi.md#numberLimitsQuery) | **GET** /num/limits/query | Reservation Limit Query
[**numberLimitsQueryByRequestId**](NumberAdministrationApi.md#numberLimitsQueryByRequestId) | **GET** /num/limits/query/{requestId} | Reservation Limit Query - Sync Timeout
[**numberOneClick**](NumberAdministrationApi.md#numberOneClick) | **PUT** /num/number/srchres/oneClick | One Click Activate 
[**numberOneClickbyRequestId**](NumberAdministrationApi.md#numberOneClickbyRequestId) | **GET** /num/number/srchres/oneClick/{requestId} | One Click Activate Polling 
[**numberQuery**](NumberAdministrationApi.md#numberQuery) | **GET** /num/number/query | Number Query
[**numberQueryByRequestId**](NumberAdministrationApi.md#numberQueryByRequestId) | **GET** /num/number/query/{requestId} | Number Query - Sync Timeout
[**numberSearch**](NumberAdministrationApi.md#numberSearch) | **PUT** /num/number/search | Number Search
[**numberSearchAndReserve**](NumberAdministrationApi.md#numberSearchAndReserve) | **PUT** /num/number/srchres | Number Search and Reserve 
[**numberSearchAndReserveByRequestId**](NumberAdministrationApi.md#numberSearchAndReserveByRequestId) | **GET** /num/number/srchres/{requestId} | Number Search and Reserve Polling 
[**numberSearchByRequestId**](NumberAdministrationApi.md#numberSearchByRequestId) | **GET** /num/number/search/{requestId} | Number Search - Sync Timeout
[**numberSpare**](NumberAdministrationApi.md#numberSpare) | **PUT** /num/status/spare | Number Status Spare
[**numberSpareByRequestId**](NumberAdministrationApi.md#numberSpareByRequestId) | **GET** /num/status/spare/{requestId} | Number Status Spare - Sync Timeout
[**numberUpdate**](NumberAdministrationApi.md#numberUpdate) | **PUT** /num/number/update | Number Update
[**numberUpdateByRequestId**](NumberAdministrationApi.md#numberUpdateByRequestId) | **GET** /num/number/update/{requestId} | Number Update - Sync Timeout
[**troubleReferralNumberQuery**](NumberAdministrationApi.md#troubleReferralNumberQuery) | **GET** /num/trq/query | Trouble Referral Number Query 
[**troubleReferralNumberQuerybyRequestId**](NumberAdministrationApi.md#troubleReferralNumberQuerybyRequestId) | **GET** /num/trq/query/{requestId} | Trouble Referral Number Query - Sync Timeout 


<a name="numberLimitsQuery"></a>
# **numberLimitsQuery**
> NumberLimitsQueryResponse numberLimitsQuery(authorization)

Reservation Limit Query

The limits resource shows the various settings around reservations. There are no input parameters to the query since they apply to the clients associated RespOrg.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token


apiInstance.numberLimitsQuery(authorization, (error, data, response) => {
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

[**NumberLimitsQueryResponse**](NumberLimitsQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberLimitsQueryByRequestId"></a>
# **numberLimitsQueryByRequestId**
> NumberLimitsQueryResponse numberLimitsQueryByRequestId(authorization, requestId)

Reservation Limit Query - Sync Timeout

This API is used if [/num/limits/query/](tag/Reservation-Limit-Query%2Fpaths%2F~1num~1limits~1query%2Fget) api returns a HTTP 202 with a RequestID in the payload. Please see the section [Polling](#section/Polling) for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.numberLimitsQueryByRequestId(authorization, requestId, (error, data, response) => {
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

[**NumberLimitsQueryResponse**](NumberLimitsQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberOneClick"></a>
# **numberOneClick**
> OneClickActivateResponse numberOneClick(authorization, body)

One Click Activate 

Using this API, user (Resp Org) can send in one click activate requests.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.OneClickActivateRequest(); // OneClickActivateRequest | 


apiInstance.numberOneClick(authorization, body, (error, data, response) => {
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
 **body** | [**OneClickActivateRequest**](OneClickActivateRequest.md)|  | 

### Return type

[**OneClickActivateResponse**](OneClickActivateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberOneClickbyRequestId"></a>
# **numberOneClickbyRequestId**
> OneClickActivateResponse numberOneClickbyRequestId(authorization, requestId)

One Click Activate Polling 

This API is used if /num/number/srchres/oneClick api returns a HTTP 202 with a RequestID (and BlkId if requested quantity was greater than 10) in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.numberOneClickbyRequestId(authorization, requestId, (error, data, response) => {
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

[**OneClickActivateResponse**](OneClickActivateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberQuery"></a>
# **numberQuery**
> NumberQueryResponse numberQuery(authorization, num)

Number Query

This API is used to query the details for a specific number. Only one number can be requested at a time, to retrieve the status and ownership information.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let num = "num_example"; // String | Dial Number to be queried


apiInstance.numberQuery(authorization, num, (error, data, response) => {
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
 **num** | **String**| Dial Number to be queried | 

### Return type

[**NumberQueryResponse**](NumberQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberQueryByRequestId"></a>
# **numberQueryByRequestId**
> NumberQueryResponse numberQueryByRequestId(authorization, requestId)

Number Query - Sync Timeout

This API is used if [/num/number/query](#tag/Number-Query%2Fpaths%2F~1num~1number~1query%2Fget) api returns a HTTP 202 with a RequestID in the payload. Please see the section [Polling](#section/Polling) for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.numberQueryByRequestId(authorization, requestId, (error, data, response) => {
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

[**NumberQueryResponse**](NumberQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberSearch"></a>
# **numberSearch**
> NumberSearchResponse numberSearch(authorization, body)

Number Search

The search action will determine if a toll free number is available (spare) and if found, will place a temporary hold on any the number. The search function has the possibility of exceeding the defined timeout for a synchronous call, and so there is a possibility that a search will return a HTTP 202 code with a RequestId that a client will use to poll for a response. If no number, NXX, or STARTING LINE NUMBER parameters are provided, the TFNR system will invoke the random search function and look for the appropriate amount of spare numbers (with or without specified NPA). If a START NXX is specified, and no spare numbers are found in that NXX, the TFNR system will select numbers from the next open NXX in the specified NPA or in any NPA if no NPA is specified. If the TFNR system is unable to find the entire quantity of numbers requested, the system will return what it found and mark the response as a \&quot;partial completion\&quot;. If the TFNR system cannot find a number specified in the NUM parameter, then no number will be returned. Duplicate numbers and RCC numbers are no longer supported by the TFNR system. After doing a search and a number has been found to be spare, a pre-reservation lock is placed on it for a period defined around reservations. During the pre-reservation period, the number is protected and can only be reserved by the same RESP ORG that did the initial search. If the number has not been reserved by the RESP ORG that did the initial search, it becomes available to anyone. If the same RESP ORG or another RESP ORG queries or searches the same number before the pre-reservation time-out occurs, an error message is returned. If the RESP ORG that submitted the original search requests submits a reservation request after the pre-reservation period has expired, it may result in an error message if another user has a lock (pre-reservation or waiting) on it or has reserved it.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.NumberSearchRequest(); // NumberSearchRequest | 


apiInstance.numberSearch(authorization, body, (error, data, response) => {
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
 **body** | [**NumberSearchRequest**](NumberSearchRequest.md)|  | 

### Return type

[**NumberSearchResponse**](NumberSearchResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberSearchAndReserve"></a>
# **numberSearchAndReserve**
> NumberSearchReserveResponse numberSearchAndReserve(authorization, body)

Number Search and Reserve 

This API is used to search for number(s) and reserve any of those number(s) which can be reserved. The schemas and request types are like the search action with a few additional fields involving the contact information and notes. When a search and reserve API request is submitted, a waiting lock is placed on the number(s) for a period defined around reservations. If the RSP-NSR is unable to fully complete a reservation request within the allotted time, a response with an error message will be returned for each number still in a waiting status. Waiting means that TFNR system is still processing the request, but does not guarantee a reservation. If any number is searched for and found, it will simultaneously be reserved.  If the quantity in the request is greater than 10 it would be accepted (202 Response) as a bulk request, for which a Bulk ID would be returned along with Request Id. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.NumberSearchReserveRequest(); // NumberSearchReserveRequest | 


apiInstance.numberSearchAndReserve(authorization, body, (error, data, response) => {
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
 **body** | [**NumberSearchReserveRequest**](NumberSearchReserveRequest.md)|  | 

### Return type

[**NumberSearchReserveResponse**](NumberSearchReserveResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberSearchAndReserveByRequestId"></a>
# **numberSearchAndReserveByRequestId**
> NumberSearchReserveResponse numberSearchAndReserveByRequestId(authorization, requestId)

Number Search and Reserve Polling 

This API is used if [/num/number/srchres](#tag/Number-Search-and-Reserve%2Fpaths%2F~1num~1number~1srchres%2Fput) api returns a HTTP 202 with a RequestID in the payload. Please see the section [Polling](#section/Polling) for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.numberSearchAndReserveByRequestId(authorization, requestId, (error, data, response) => {
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

[**NumberSearchReserveResponse**](NumberSearchReserveResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberSearchByRequestId"></a>
# **numberSearchByRequestId**
> NumberSearchResponse numberSearchByRequestId(authorization, requestId)

Number Search - Sync Timeout

This API is used if [/num/number/search](#tag/Number-Search%2Fpaths%2F~1num~1number~1search%2Fput) api returns a HTTP 202 with a RequestID in the payload. Please see the section [Polling](#section/Polling) for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.numberSearchByRequestId(authorization, requestId, (error, data, response) => {
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

[**NumberSearchResponse**](NumberSearchResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberSpare"></a>
# **numberSpare**
> NumberSpareResponse numberSpare(authorization, body)

Number Status Spare

This API is used to request for a dial number to be spared. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.NumberSpareRequest(); // NumberSpareRequest | 


apiInstance.numberSpare(authorization, body, (error, data, response) => {
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
 **body** | [**NumberSpareRequest**](NumberSpareRequest.md)|  | 

### Return type

[**NumberSpareResponse**](NumberSpareResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberSpareByRequestId"></a>
# **numberSpareByRequestId**
> NumberSpareResponse numberSpareByRequestId(authorization, requestId)

Number Status Spare - Sync Timeout

This API is used if /num/status/spare API returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.numberSpareByRequestId(authorization, requestId, (error, data, response) => {
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

[**NumberSpareResponse**](NumberSpareResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberUpdate"></a>
# **numberUpdate**
> NumberUpdateResponse numberUpdate(authorization, body)

Number Update

The number update API is used to modify the contact information, notes, or the controlling RespOrg. Before calling this API it is REQUIRED to invoke /number/query for the same number.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.NumberUpdateRequest(); // NumberUpdateRequest | 


apiInstance.numberUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**NumberUpdateRequest**](NumberUpdateRequest.md)|  | 

### Return type

[**NumberUpdateResponse**](NumberUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="numberUpdateByRequestId"></a>
# **numberUpdateByRequestId**
> NumberUpdateResponse numberUpdateByRequestId(authorization, requestId)

Number Update - Sync Timeout

This API is used if [/num/number/update](#tag/Number-Update%2Fpaths%2F~1num~1number~1update%2Fput) api returns a HTTP 202 with a RequestID in the payload. Please see the section [Polling](#section/Polling) for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.numberUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**NumberUpdateResponse**](NumberUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="troubleReferralNumberQuery"></a>
# **troubleReferralNumberQuery**
> TroubleNumberQueryResponse troubleReferralNumberQuery(authorization, numList)

Trouble Referral Number Query 

This API is used to retrieve the trouble referral number associated with specific number(s) or RESP ORG. Users can request up to ten (10) dial numbers in a single request. This call provides information only, and cannot be used to change the trouble referral number associated with the RESP ORG.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let numList = ["numList_example"]; // [String] | dialed Number


apiInstance.troubleReferralNumberQuery(authorization, numList, (error, data, response) => {
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
 **numList** | [**[String]**](String.md)| dialed Number | 

### Return type

[**TroubleNumberQueryResponse**](TroubleNumberQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="troubleReferralNumberQuerybyRequestId"></a>
# **troubleReferralNumberQuerybyRequestId**
> TroubleNumberQueryResponse troubleReferralNumberQuerybyRequestId(authorization, requestId)

Trouble Referral Number Query - Sync Timeout 

This API is used if /num/trq/query API returns a HTTP 202 with a RequestID in the payload. Please see the section Polling for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.NumberAdministrationApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.troubleReferralNumberQuerybyRequestId(authorization, requestId, (error, data, response) => {
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

[**TroubleNumberQueryResponse**](TroubleNumberQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

