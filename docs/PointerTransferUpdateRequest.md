# TfnrApIs.PointerTransferUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**num** | **String** | Dialed number of the record  | 
**effDtTm** | **String** | Effective date and time of the records | 
**srcEffDtTm** | **String** | Effective date and time of the records - (eff date with time part or eff date without time) : without NOW | 
**tempName** | **String** |  | 
**reqSntFrom** | [**ReqSntFrom**](ReqSntFrom.md) | Functional area from where the Customer Record requests were initiated from | 
**cmd** | [**Cmd**](Cmd.md) |  | 
**referral** | [**BoolYN**](BoolYN.md) |  | [optional] 
**endInterceptDt** | **String** |  | [optional] 
**priority** | [**BoolYN**](BoolYN.md) |  | [optional] 
**dueDt** | **String** | Due Date | [optional] 
**hldIndFlag** | [**BoolYN**](BoolYN.md) | Indicates whether or not a hold has been placed on the due date | 
**svcOrderNum** | **String** | Service Order Number. 13 bytes identifier. Range can be from 4 to 13 bytes. First character must be alphabetic. Second thru twelfth characters must be alphanumeric thirteenth character must be alphabetic. Required unless sf field is used either sf or so is required  | [optional] 
**suppFormNum** | **String** | Supplemental Form Number. 6 bytes text string. Maximum of 6 bytes alphanumeric. | [optional] 
**notes** | **String** | Notes. Naximum of 151 bytes. Any notes on the Service Order or Supplemental Form which need to be stored and for which no specific field exists  | [optional] 
**co** | **String** | Company that sold SMS access | [optional] 
**agent** | **String** | On Line Agent for Customer. 5 bytes text string. Alphanumeric values only | [optional] 
**onAccCust** | **String** | On-line Access Customer. Alphanumeric values only  | [optional] 
**newRespOrgId** | **String** | New Responsible Organization  | [optional] 
**endSubAddr** | **String** | End Subscriber Address(formerly Listing Address) 75 bytes string | [optional] 
**conName** | **String** | Name of ContactNo numbers allowed | [optional] 
**conTel** | **String** | Contact Phone Number | [optional] 
**endSub** | **[String]** | End Subscriber. Not allowed for automation. 75 bytes text string | [optional] 
**destNums** | [**[DestNums]**](DestNums.md) | Destination Telephone Numbers list | 
**custRecCompPart** | [**CustRecCompPart**](CustRecCompPart.md) |  | [optional] 


