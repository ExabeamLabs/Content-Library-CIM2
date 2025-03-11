#### Parser Content
```Java
{
Name = cisco-netsec-json-alert-trigger-success-ids_alert
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [ """"eventType":""", """"IDS Alert"""", """"signature":""", """"classification":""" ]
  Fields = [
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.srcIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destIp,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.clientMac,exa_field_name=src_mac""",
    """exa_json_path=$.eventType,exa_field_name=alert_type""",
    """exa_json_path=$.priority,exa_field_name=alert_severity""",
    """exa_json_path=$.protocol,exa_field_name=protocol""",
    """exa_json_path=$.ruleId,exa_field_name=rule_id""",
    """exa_json_path=$.blocked,exa_field_name=blocked""",
    """exa_json_path=$.message,exa_field_name=alert_name"""
  ]
  ParserVersion = "v1.0.0"


}
```