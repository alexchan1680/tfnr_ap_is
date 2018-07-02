# TfnrApIs.SessionApi

All URIs are relative to *https://api-devp-tfnregistry.somos.com/v1/ip*

Method | HTTP request | Description
------------- | ------------- | -------------
[**sessionClose**](SessionApi.md#sessionClose) | **DELETE** /sec/session/close | Session Close
[**sessionOpen**](SessionApi.md#sessionOpen) | **POST** /sec/session/open | Session Open


<a name="sessionClose"></a>
# **sessionClose**
> SessionCloseResponse sessionClose(authorization)

Session Close

The session close API provides a graceful way to end an API session. The alternative is to let the session token expire. There are some considerations in restarting a session that has timed out, so it is recommended to close the session explicitly. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.SessionApi();

let authorization = "authorization_example"; // String | Bearer access_token


apiInstance.sessionClose(authorization, (error, data, response) => {
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

[**SessionCloseResponse**](SessionCloseResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sessionOpen"></a>
# **sessionOpen**
> SessionOpenResponse sessionOpen(body)

Session Open

This API provides the capability to open a session for calling APIs and to obtain the client key and secret. This API requires a username and password, and includes an optional field to request UI permissions for the user. Behind the scenes, the session/open API calls the /token API on behalf of the user to obtain an OAuth token. Every client must invoke the session/open API at least once to obtain a key and secret that are required to make the /token OAuth API call. It is the client&#39;s responsibility to refresh an existing OAuth token (Refresh Grant Type), or obtain a new token (Password Grant Type) as needed.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.SessionApi();

let body = new TfnrApIs.SessionOpenRequest(); // SessionOpenRequest | 


apiInstance.sessionOpen(body, (error, data, response) => {
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
 **body** | [**SessionOpenRequest**](SessionOpenRequest.md)|  | 

### Return type

[**SessionOpenResponse**](SessionOpenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

