#### Parser Content
```Java
{
Name = zeek-z-json-http-session-status
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ 
""""status_code":"""
""""trans_depth":"""
""""id.resp_h":"""
""""resp_mime_types""""
]
  Fields = [
    """exa_json_path=$.ts,exa_field_name=time""",
    """exa_json_path=$.uid,exa_field_name=connection_id""",
    """exa_regex="id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="id\.orig_p\\?"+:({src_port}\d+)""",
    """exa_regex="id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_regex="id\.resp_p\\?"+:({dest_port}\d+)""",
    """exa_json_path=$.proto,exa_field_name=protocol""",
    """exa_json_path=$._system_name,exa_field_name=host""",
    """exa_json_path=$.status_code,exa_field_name=http_response_code""",
    """exa_json_path=$.resp_mime_types[:1],exa_field_name=mime""",
    """exa_json_path=$.resp_fuids[:1],exa_field_name=file_id""",
    """exa_json_path=$.status_msg,exa_field_name=additional_info""",
    """exa_json_path=$.method,exa_field_name=method""",
    """exa_json_path=$.uri,exa_regex=({uri_path}[^"\?]+?)\s*({uri_query}\?[^"]+?)?\s*"""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent"""
  ]


}
```