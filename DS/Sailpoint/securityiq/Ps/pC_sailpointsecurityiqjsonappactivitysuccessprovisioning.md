#### Parser Content
```Java
{
Name = sailpoint-securityiq-json-app-activity-success-provisioning
  Conditions = [ """"type":"PROVISIONING"""", """"action":""", """"operation":""" ]
  Vendor = "Sailpoint"
  Product = "SecurityIQ"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.created,exa_field_name=time""",
    """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.type,exa_field_name=category""",
    """exa_json_path=$.target.name,exa_field_name=target""",
    """exa_json_path=$.attributes.cloudAppName,exa_field_name=app""",
    """exa_json_path=$.operation,exa_field_name=operation""",
    """exa_json_path=$.attributes.previousValue,exa_field_name=old_value""",
    """exa_json_path=$.attributes.accountName,exa_regex=(({user_dn}(((CN|cn|uid)=[^"]+?),)?(({user_ou}(OU|ou)[^"]+?)?(DC|dc)=[\w-]+))|({account_id}[^"]+?)\\?")""",
    """exa_json_path=$.attributes.attributeName,exa_field_name=additional_info""",
    """exa_json_path=$.status,exa_field_name=result""",
    """exa_json_path=$.technicalName,exa_field_name=event_name""",
  ]
  ParserVersion = "v1.0.0"


}
```