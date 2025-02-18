#### Parser Content
```Java
{
Name = servicenow-s-json-http-session-success-transcation
  ParserVersion = v1.0.0
  Vendor = ServiceNow
  Product = ServiceNow
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"business_rule_count":""", """"type":""", """"sys_created_on":""", """"sys_created_by":""", """transaction_pattern":""" ]
  Fields = [
    """exa_json_path=$.sys_created_on,exa_field_name=time"""
    """exa_json_path=$.sys_created_by,exa_field_name=user"""
    """exa_json_path=$.protocol,exa_field_name=protocol"""
    """exa_json_path=$.remote_ip,exa_field_name=src_ip""" 
    """exa_json_path=$.link,exa_field_name=url"""
    """exa_json_path=$.user_agent,exa_field_name=user_agent"""
    """exa_json_path=$.output_length,exa_field_name=bytes""" 
  ]


}
```