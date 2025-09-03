#### Parser Content
```Java
{
Name = zeek-z-json-http-session-hoststatus
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ 
""""id.orig_h":"""
""""id.resp_h":"""
""""host":"""
""""method":"""
]
  Fields = [
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.uid,exa_field_name=connection_id""",
    """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
    """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
    """exa_json_path=$.host,exa_regex=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^\s"]+\.[^\s"]+)|({host}[\w.-]+))""",
    """exa_json_path=$._system_name,exa_field_name=host""",
    """exa_json_path=$.uri,exa_regex=({uri_path}[^"\?]+?)\s*({uri_query}\?[^"]+?)?\s*""",
    """exa_regex="uri":"({uri_path}[^"\?]+?)\s*({uri_query}\?[^"]+?)?\s*"""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent""",
    """exa_json_path=$.status_code,exa_field_name=http_response_code""",
    """exa_json_path=$.method,exa_field_name=method""",
    """exa_json_path=$.resp_mime_types[:1],exa_field_name=mime"""
  ]


}
```