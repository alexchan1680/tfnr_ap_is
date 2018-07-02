# TfnrApIs.PasswordApi

All URIs are relative to *https://api-devp-tfnregistry.somos.com/v1/ip*

Method | HTTP request | Description
------------- | ------------- | -------------
[**passwordForgot**](PasswordApi.md#passwordForgot) | **POST** /sec/usr/forgotPassword | Forgot Password 
[**passwordForgotbyRequestId**](PasswordApi.md#passwordForgotbyRequestId) | **GET** /sec/usr/forgotPassword/{requestId} | Forgot Password - Sync Timeout 
[**passwordReset**](PasswordApi.md#passwordReset) | **POST** /sec/usr/resetPassword | Password Reset 
[**passwordResetbyRequestId**](PasswordApi.md#passwordResetbyRequestId) | **GET** /sec/usr/resetPassword/{requestId} | Password Reset - Sync Timeout 
[**passwordUpdate**](PasswordApi.md#passwordUpdate) | **PUT** /sec/password/update | Password Update
[**passwordUpdateByRequestId**](PasswordApi.md#passwordUpdateByRequestId) | **GET** /sec/password/update/{requestId} | Password Update - Sync Timeout


<a name="passwordForgot"></a>
# **passwordForgot**
> PasswordForgetResponse passwordForgot(body)

Forgot Password 

This API is used to request the system for a reset password link.  The call will assume that the user has forgotten their password, but knows their login id.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PasswordApi();

let body = new TfnrApIs.PasswordForgetRequest(); // PasswordForgetRequest | 


apiInstance.passwordForgot(body, (error, data, response) => {
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
 **body** | [**PasswordForgetRequest**](PasswordForgetRequest.md)|  | 

### Return type

[**PasswordForgetResponse**](PasswordForgetResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="passwordForgotbyRequestId"></a>
# **passwordForgotbyRequestId**
> PasswordForgetResponse passwordForgotbyRequestId(requestId)

Forgot Password - Sync Timeout 

This API is used to poll the status of forgot password request. It is used if /usr/forgotPassword API returns an HTTP 202 with a RequestID in the payload.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PasswordApi();

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.passwordForgotbyRequestId(requestId, (error, data, response) => {
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
 **requestId** | **Number**| RequestId returned due to timeout | 

### Return type

[**PasswordForgetResponse**](PasswordForgetResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="passwordReset"></a>
# **passwordReset**
> PasswordResetResponse passwordReset(body)

Password Reset 

This API allows the User to reset their password. It is invoked through the URL link that is made available to the User (primarily through an email) on submitting the Forgot Password request.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PasswordApi();

let body = new TfnrApIs.PasswordResetRequest(); // PasswordResetRequest | 


apiInstance.passwordReset(body, (error, data, response) => {
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
 **body** | [**PasswordResetRequest**](PasswordResetRequest.md)|  | 

### Return type

[**PasswordResetResponse**](PasswordResetResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="passwordResetbyRequestId"></a>
# **passwordResetbyRequestId**
> PasswordResetResponse passwordResetbyRequestId(requestId)

Password Reset - Sync Timeout 

This API allows the User to reset their password. If the /usr/resetPassword API returns an HTTP 202 with a RequestID in the payload, then this API can be invoked for polling. 

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PasswordApi();

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.passwordResetbyRequestId(requestId, (error, data, response) => {
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
 **requestId** | **Number**| RequestId returned due to timeout | 

### Return type

[**PasswordResetResponse**](PasswordResetResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="passwordUpdate"></a>
# **passwordUpdate**
> PasswordUpdateResponse passwordUpdate(authorization, body)

Password Update

This API is used to update a client&#39;s password. The reason for the update might be voluntary or required due to a password reset/password expired.    1. Voluntary: Provide the 3 values and server responds with either a suceess or failed response.    2. Required Update: Before calling the /password/update, it is required to invoke the /session/open other wise the system will return error.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PasswordApi();

let authorization = "authorization_example"; // String | Bearer access_token

let body = new TfnrApIs.PasswordUpdateRequest(); // PasswordUpdateRequest | 


apiInstance.passwordUpdate(authorization, body, (error, data, response) => {
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
 **body** | [**PasswordUpdateRequest**](PasswordUpdateRequest.md)|  | 

### Return type

[**PasswordUpdateResponse**](PasswordUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="passwordUpdateByRequestId"></a>
# **passwordUpdateByRequestId**
> PasswordUpdateResponse passwordUpdateByRequestId(authorization, requestId)

Password Update - Sync Timeout

This API is used if [/password/update](#tag/Password-Update%2Fpaths%2F~1sec~1password~1update%2Fput) api returns a HTTP 202 with a RequestID in the payload. Please see the section [Polling](#section/Polling) for more information on how to do the polling.

### Example
```javascript
import TfnrApIs from 'tfnr_ap_is';

let apiInstance = new TfnrApIs.PasswordApi();

let authorization = "authorization_example"; // String | Bearer access_token

let requestId = 789; // Number | RequestId returned due to timeout


apiInstance.passwordUpdateByRequestId(authorization, requestId, (error, data, response) => {
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

[**PasswordUpdateResponse**](PasswordUpdateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

