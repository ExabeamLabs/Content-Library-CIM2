#### Parser Content
```Java
{
Name = armis-a-json-alert-trigger-success-systempolicyviolation
  ParserVersion = v1.0.0
  Vendor = Armis
  Product = Armis Platform
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  ExtractionType = json
  Conditions = [ """"alertId": """, """"activities": """, """"status": """, """"type": "System Policy Violation""""  ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.title,exa_field_name=alert_name""",
    """exa_regex=({alert_type}System Policy Violation)""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.status,exa_field_name=alert_status""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_json_path=$.alertId,exa_field_name=alert_id""",
    """exa_json_path=$.deviceIds,exa_field_name=device_id_list""",
    ]


}
```