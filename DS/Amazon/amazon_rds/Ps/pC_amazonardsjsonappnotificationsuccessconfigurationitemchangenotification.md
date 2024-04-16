#### Parser Content
```Java
{
Name = amazon-ards-json-app-notification-success-configurationitemchangenotification
 Vendor = Amazon
 Product = Amazon RDS
 ExtractionType = json
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 ParserVersion = v1.0.0
 Conditions = [""""messageType":"ConfigurationItemChangeNotification"""", """"configurationItemDiff":""",  """"Relationships.""", """"changeType":""", """"notificationCreationTime":""" ]
 Fields = [
   """exa_json_path=$..changedProperties..previousValue,exa_field_name=old_value""",
   """exa_json_path=$.notificationCreationTime,exa_field_name=time""",
   """exa_json_path=$.messageType,exa_field_name=event_name""",
   """exa_json_path=$.configurationItemDiff.changedProperties..changeType,exa_field_name=operation""",
   """exa_json_path=$.configurationItem.awsAccountId,exa_field_name=account_id""",
   """exa_json_path=$.configurationItem.relationships[0].resourceType,exa_field_name=resource_type""",
   """exa_json_path=$..ARN,exa_field_name=policy_arn""",
 ]


}
```