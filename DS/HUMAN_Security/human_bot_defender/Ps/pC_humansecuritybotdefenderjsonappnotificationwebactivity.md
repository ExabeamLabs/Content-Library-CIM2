#### Parser Content
```Java
{
Name = humansecurity-botdefender-json-app-notification-webactivity
  Vendor = HUMAN Security
  Product = HUMAN Bot Defender
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"client_ip":""", """"http_method":""", """"http_status":""", """"px_app_id":""" ]
  Fields = [
    """exa_json_path=$.client_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.domain,exa_field_name=domain""",
    """exa_json_path=$.http_method,exa_field_name=method""",
    """exa_json_path=$.http_status,exa_field_name=http_response_code""",
    """exa_json_path=$.os_name,exa_field_name=os""",
    """exa_json_path=$.os_version,exa_field_name=os_version""",
    """exa_json_path=$.path,exa_field_name=path""",
    """exa_json_path=$.px_app_id,exa_field_name=app_id""",
    """exa_json_path=$.risk_score,exa_field_name=risk_score""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent"""
  ]
  ParserVersion = "v1.0.0"


}
```