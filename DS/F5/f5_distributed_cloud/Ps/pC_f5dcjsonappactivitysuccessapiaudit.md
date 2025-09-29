#### Parser Content
```Java
{
Name = f5-dc-json-app-activity-success-apiaudit
  Vendor = F5
  Product = F5 Distributed Cloud
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"req_path":""", """"namespace":""", """.req_body":""", """"API Audit""", """"user_agent":""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.user_agent,exa_field_name=user_agent"""
    """exa_json_path=$.method,exa_field_name=method"""
    """exa_json_path=$.rsp_code,exa_field_name=http_response_code"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.req_path,exa_field_name=uri_path""",
    """exa_json_path=$.rpc,exa_field_name=operation""",
    """exa_json_path=$.req_size,exa_field_name=bytes_in""",
    """exa_json_path=$.rsp_size,exa_field_name=bytes_out""",
    """exa_json_path=$.transport,exa_field_name=protocol""",
    """exa_json_path=$.tenant,exa_field_name=tenant_id""",
    """exa_regex=(.object_name":\s*"({object_name}[^"]+))""",
    """exa_regex=(.object_type":\s*"({object_type}[^"]+))""",
    """exa_regex=(.object_uid":\s*"({object_id}[^"]+))""",
    """exa_regex=(.oper_name":\s*"({action}[^"]+))""",
    """exa_json_path=$.namespace,exa_field_name=app_type""",
    """exa_regex=(.user_message":\s*"({additional_info}[^"]+))"""
  ]
  ParserVersion = v1.0.0


}
```