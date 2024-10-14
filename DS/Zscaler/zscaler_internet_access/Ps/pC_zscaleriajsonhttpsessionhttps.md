#### Parser Content
```Java
{
Name = "zscaler-ia-json-http-session-https"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ExtractionType = json
Conditions = [
""","ologin":""""
""","cip":""""
""","url":""""
""","urlsupercat":""""
""","reqdatasize":"""
]
Fields = [
  """exa_json_path=$.time,exa_field_name=time""",
  """exa_json_path=$.ologin,exa_regex=({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@[^@\s"]+)""",
  """exa_json_path=$.cip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
 """exa_json_path=$.proto,exa_field_name=protocol""",
 """exa_json_path=$.reqmethod,exa_field_name=method""",
 """exa_json_path=$.url,exa_field_name=url""",
 """exa_json_path=$.url,exa_regex=(?:[^:]+:\/+)?({web_domain}[^\/:\s"]+)({uri_path}\/[^\?"]+)?({uri_query}\?[^"]+)?"""
"""exa_json_path=$.respcode,exa_field_name=http_response_code""",
"""exa_json_path=$.sip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""exa_json_path=$.action,exa_field_name=action""",
"""exa_json_path=$.reason,exa_field_name=proxy_action""",
"""exa_json_path=$.urlsupercat,exa_field_name=category""",
"""exa_json_path=$.ua,exa_field_name=user_agent""",
"""exa_json_path=$.referer,exa_field_name=referrer""",
"""exa_json_path=$.reqdatasize,exa_field_name=bytes_out""",
"""exa_json_path=$.respdatasize,exa_field_name=bytes_in""",
"""exa_json_path=$.fileclass,exa_field_name=mime"""
]
ParserVersion = "v1.0.0"


}
```