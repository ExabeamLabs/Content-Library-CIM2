#### Parser Content
```Java
{
Name = amazon-ards-json-app-notification-datamessage
 Vendor = Amazon
 Product = Amazon RDS
 ExtractionType = json
 TimeFormat = ["yyyy-MM-dd HH:mm:ss", "epoch_sec"]
 ParserVersion = v1.0.0
 Conditions = [""""messageType":"DATA_MESSAGE"""",  """"subscriptionFilters":""", """"logEvents":{"message":""" ]
 Fields = [
   """exa_json_path=$.messageType,exa_field_name=object""",
   """exa_json_path=$.owner,exa_field_name=owner_id""",
   """exa_json_path=$.logGroup,exa_field_name=log_source""",
   """exa_json_path=$.logStream,exa_field_name=service_name""",
   """exa_json_path=$.subscriptionFilters,exa_field_name=rule""",
   """exa_json_path=$.logEvents.message,exa_field_name=additional_info""",
   """exa_json_path=$.AccountName,exa_field_name=account_name""",
   """exa_json_path=$.Environment,exa_field_name=environment""",
   """exa_json_path=$.logEvents.message,exa_regex=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*UTC"""
   """exa_json_path=$.logEvents.message,exa_regex=({time}\d{10})\d+,({cluster_name}[^,]+),({user}[^,]+),({host}[^,]+),({connection_id}[^,]+),({session_id}[^,]+),({action}[^,]+),,,({error_code}[^,]+)"""
 ]


}
```