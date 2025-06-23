#### Parser Content
```Java
{
Name = portkey-p-json-app-activity-success-portkey
  Product = Portkey
  Vendor = Portkey
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"portkeyHeaders":""", """"body":""", """"messages":""", """"role":""", """"content":""" ]
  Fields = [
    """exa_json_path=$.metrics.created_at,exa_field_name=time""",
    """exa_json_path=$.request.headers.host,exa_field_name=host""",
    #"""exa_json_path=$.metrics[?(@.metadata__key[0] == '_user')].metadata__value[0],exa_regex=^(({full_name}\w+[\s\,]+\w+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$.request.body.model,exa_field_name=resource_name""",
    """exa_json_path=$.request.body.messages,exa_field_name=additional_info""",
    """exa_json_path=$.request.body.messages[?(@.role == 'user')].role,exa_field_name=role""",
    """exa_json_path=$.request.body.messages[?(@.role == 'user')].content,exa_field_name=status_msg"""
  ]
  ParserVersion = "v1.0.0"


}
```