#### Parser Content
```Java
{
Name = amazon-ards-json-app-notification-success-configurationitemstatus
 Vendor = Amazon
 Product = Amazon RDS
 ExtractionType = json
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 ParserVersion = v1.0.0
 Conditions = [""""configurationItemStatus":""",  """"configurationStateId":""", """"configurationItemCaptureTime":""" ]
 Fields = [
   """exa_json_path=$.configurationItems[0].configurationItemCaptureTime,exa_field_name=time""",
   """exa_json_path=$.configurationItems[0].configurationItemStatus,exa_field_name=operation""",
   """exa_json_path=$.configurationItems[0].awsAccountId,exa_field_name=account_id""",
   """exa_json_path=$.configurationItems..relationships[0].resourceType,exa_field_name=resource_type""",
   """exa_json_path=$.configurationItems[0].ARN,exa_field_name=policy_arn""",
 ]


}
```