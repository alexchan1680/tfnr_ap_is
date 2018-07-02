# TfnrApIs.OneClickActivateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**qty** | **Number** | Quantity of numbers to be searched for. Valid range 1-500 | 
**conName** | **String** | Name of Contact. No numbers allowed | 
**conPhone** | **String** | Contact Person&#39;s phone number | 
**shrtNotes** | **String** | Additional Information | [optional] 
**numList** | **[String]** |  | [optional] 
**npa** | [**Npa**](Npa.md) |  | [optional] 
**nxx** | **String** | Specifies the NXX where search should start. Valid values are 000 to 999 | [optional] 
**line** | **String** | Staring Line - Specifies the last 4 characters of phone number. | [optional] 
**cons** | [**Cons**](Cons.md) |  | [optional] 
**effDtTm** | **String** | Effective date and time of the records | 
**timeZone** | [**TimeZone**](TimeZone.md) |  | [optional] 
**tempName** | **String** |  | 
**numTermLine** | **Number** |  | 
**svcOrderNum** | **String** | Service Order Number. 13 bytes identifier. Range can be from 4 to 13 bytes. First character must be alphabetic. Second thru twelfth characters must be alphanumeric thirteenth character must be alphabetic. Required unless sf field is used either sf or so is required  | 


