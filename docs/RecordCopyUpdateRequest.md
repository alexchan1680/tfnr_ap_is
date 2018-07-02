# TfnrApIs.RecordCopyUpdateRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**num** | **String** | Dialed number of the record  | 
**effDtTm** | **String** | Effective date and time of the records | 
**srcEffDtTm** | **String** | Effective date and time of the records | 
**reqSntFrom** | [**ReqSntFrom**](ReqSntFrom.md) | Functional area from where the Customer Record requests were initiated from | 
**cmd** | [**Cmd**](Cmd.md) |  | 
**priority** | [**BoolYN**](BoolYN.md) |  | [optional] 
**interLTCar** | **[String]** | Interlata Carrier. 7 bytes text string. Format is 3-letter (alpha) and 4-digit (numeric)  | [optional] 
**intraLTCar** | **[String]** | Intralata Carrier. 7 bytes text string. Format is 3-letter (alpha) and 4-digit (numeric)  | [optional] 
**dueDt** | **String** | Due Date | [optional] 
**hldIndFlag** | [**BoolYN**](BoolYN.md) | Indicates whether or not a hold has been placed on the due date | 
**svcOrderNum** | **String** | Service Order Number. 13 bytes identifier. Range can be from 4 to 13 bytes. First character must be alphabetic. Second thru twelfth characters must be alphanumeric thirteenth character must be alphabetic. Required unless sf field is used either sf or so is required  | [optional] 
**suppFormNum** | **String** | Supplemental Form Number. 6 bytes text string. Maximum of 6 bytes alphanumeric. | [optional] 
**notes** | **String** | Notes. Naximum of 151 bytes. Any notes on the Service Order or Supplemental Form which need to be stored and for which no specific field exists  | [optional] 
**agent** | **String** | On Line Agent for Customer. 5 bytes text string. Alphanumeric values only | [optional] 
**co** | **String** | Company that sold SMS access | [optional] 
**onAccCust** | **String** | On-line Access Customer. Alphanumeric values only  | [optional] 
**newRespOrgId** | **String** | New Responsible Organization  | 
**endSubAddr** | **String** | End Subscriber Address(formerly Listing Address) 75 bytes string | [optional] 
**conName** | **String** | Name of Contact. No numbers allowed | [optional] 
**conTel** | **String** | Contact Phone Number | [optional] 
**aos** | [**Aos**](Aos.md) |  | 
**endSub** | **[String]** | End Subscriber. Not allowed for automation. 75 bytes text string | [optional] 
**destNums** | [**[DestNums]**](DestNums.md) |  | 
**numRoutPath** | **String** |  | [optional] 
**custRecCompPart** | [**CustRecCompPart**](CustRecCompPart.md) |  | [optional] 
**cprSectName** | [**[CprSectName]**](CprSectName.md) |  | [optional] 
**priInterLT** | **String** | Primary InterLATA Carrier | [optional] 
**priIntraLT** | **String** |  | [optional] 
**tmZn** | [**TimeZone**](TimeZone.md) |  | [optional] 
**lbl** | [**[Lbl]**](Lbl.md) | Label name Array. Not allowed for automation. Not allowed with Pointer record | [optional] 


