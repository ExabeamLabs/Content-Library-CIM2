#### Parser Content
```Java
{
Name = "microsoft-365defender-json-alert-trigger-success-behaviorinfo"
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"category":"AdvancedHunting-BehaviorInfo"""", """"operationName":"Publish"""", """"BehaviorId":"""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"tenantId":"({tenant_id}[^"]+)"""",
    """"(C|c)ategory":"({alert_type}[^"]+)"""",
    """"ActionType":"({event_name}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """"ServiceSource":"({service_name}[^"]+)"""",
    """"Categories":"\[({categories}[^\]]+)"""",
    """"AccountUpn":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"DetectionSource":"({alert_source}[^"]+)"""",
    """exa_regex="Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$..tenantId,exa_field_name=tenant_id""",
    """exa_json_path=$..category,exa_field_name=alert_type""",
    """exa_json_path=$..Category,exa_field_name=alert_type""",
    """exa_json_path=$..ActionType,exa_field_name=event_name""",
    """exa_json_path=$..description,exa_field_name=additional_info""",
    """exa_json_path=$..ServiceSource,exa_field_name=service_name""",
    """exa_json_path=$..Categories,exa_field_name=categories""",
    """exa_json_path=$..DetectionSource,exa_field_name=alert_source""",
    """exa_json_path=$..AccountUpn,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=!Contains(tolower($..AccountUpn), "null")"""
  ]
  ParserVersion = "v1.0.0"


}
```