# TfnrApIs.OauthResponse

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**oauthToken** | **String** | This token is valid for 60 mins. and should be passed as &#39;Authorization: Bearer oauthToken&#39; header when invoking the APIs | [optional] 
**refreshToken** | **String** | This token is valid for 24hrs. and should be used for obtaining a new token using the OAuth 2.0 refresh_grant flow. | [optional] 
**clientKey** | **String** | Client Key can be used for OAuth2.0 password and refresh grants. This key never expires unless revoked by the administrator. Never share your client key and secret with others. | [optional] 
**clientSecret** | **String** | Client Secret can be used for OAuth2.0 password and refresh grants. This key never expires unless revoked by the administrator. Never share your client key and secret with others. | [optional] 
**scope** | **String** | This value is always &#39;default&#39; | [optional] 
**tokenType** | **String** | This value is always &#39;Bearer&#39; | [optional] 
**expiresIn** | **Number** | Number of seconds the token is valid. | [optional] 


