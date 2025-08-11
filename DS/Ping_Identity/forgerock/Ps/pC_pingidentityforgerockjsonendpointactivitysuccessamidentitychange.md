#### Parser Content
```Java
{
Name = "pingidentity-forgerock-json-endpoint-activity-success-amidentitychange"
  Vendor = "Ping Identity"
  Product = "ForgeRock"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ExtractionType = json
  Conditions = [ """"eventName":"AM-IDENTITY-CHANGE"""", """"operation":"""", """"changedFields":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.eventName,exa_field_name=event_name"""  
    """exa_json_path=$.transactionId,exa_field_name=message_id"""
    """exa_json_path=$.runAs,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,dc=({domain}[^,]+),"""
    """exa_json_path=$.objectId,exa_regex=uid=({object_id}[^,]+),"""
    """exa_json_path=$.operation,exa_field_name=operation"""
    """exa_json_path=$.realm,exa_field_name=realm"""
    """exa_json_path=$.component,exa_field_name=category"""
    """exa_json_path=$.changedFields,exa_field_name=additional_info"""
  ]
  ParserVersion = "v1.0.0"


}
```