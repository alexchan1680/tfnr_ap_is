# TfnrApIs.DisconnectUpdatePointerRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**num** | **String** | Dialed number of the record Format is npanxxxxxx. 10 character string. | 
**effDtTm** | **String** | Effective date and time of the records | [optional] 
**srcEffDtTm** | **String** | Effective date and time of the recordsISO 8601 | 
**tempName** | **String** | This is a 15 byte text field (starts with *) containing the Template  | [optional] 
**newRespOrgId** | **String** | New Responsible Organization  | [optional] 
**reqSntFrom** | [**ReqSntFrom**](ReqSntFrom.md) | Functional area from where the Customer Record requests were initiated from | 
**cmd** | [**Cmd**](Cmd.md) |  | 
**priority** | **String** | Priority of the Update. optional 1 byte identifier.H -High.The value �H� is the only allowed value at this time.When priority&#x3D;H, then effective date of customer record must equal �NOW� or today�s date; and your Logon ID must have High Priority CR Update permission defined within the SMS/800 system�s HPU screen for the customer record�s Resp Org Entity | [optional] 
**referral** | [**BoolYN**](BoolYN.md) |  | 
**endInterceptDt** | **String** |  | 
**dueDt** | **String** | Due Date | [optional] 
**hldIndFlag** | [**BoolYN**](BoolYN.md) | Indicates whether or not a hold has been placed on the due date | 
**svcOrderNum** | **String** | Service Order Number. 13 bytes identifier. Range can be from 4 to 13 bytes. First character must be alphabetic. Second thru twelfth characters must be alphanumeric thirteenth character must be alphabetic. Required unless sf field is used either sf or so is required  | [optional] 
**suppFormNum** | **String** | Supplemental Form Number. 6 bytes text string. Maximum of 6 bytes alphanumeric. | [optional] 
**notes** | **String** | Notes. Naximum of 151 bytes. Any notes on the Service Order or Supplemental Form which need to be stored and for which no specific field exists  | [optional] 
**agent** | **String** | On Line Agent for Customer. 5 bytes text string. Alphanumeric values only | [optional] 
**co** | **String** | Company that sold SMS access | [optional] 
**onAccCust** | **String** | On-line Access Customer. Alphanumeric values only  | [optional] 
**endSubAddr** | **String** | End Subscriber Address(formerly Listing Address) 75 bytes string | [optional] 
**conName** | **String** | Name of Contact. No numbers allowed | [optional] 
**conTel** | **String** | Contact Phone Number | [optional] 
**aos** | [**Aos**](Aos.md) |  | [optional] 
**endSub** | **[String]** | End Subscriber. Not allowed for automation. 75 bytes text string | [optional] 
**destNums** | [**[DestNums]**](DestNums.md) | Destination Telephone Numbers list | 
**custRecCompPart** | [**CustRecCompPart**](CustRecCompPart.md) |  | [optional] 


