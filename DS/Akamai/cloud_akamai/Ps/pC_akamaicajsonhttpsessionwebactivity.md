#### Parser Content
```Java
{
Name = akamai-ca-json-http-session-webactivity
  ParserVersion = v1.0.0
  Vendor = Akamai
  Product = Cloud Akamai
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""reqPort":""""
""""reqHost":""""
""""status"""
""""reqPath":"""" 
]
ExtractionType = json
  Fields = [
    """exa_json_path=$.start,exa_regex=({time}\d{10})""",
    """exa_json_path=$..proto,exa_field_name=protocol""",
    """exa_json_path=$..status,exa_field_name=http_response_code""",
    """exa_json_path=$..reqTimeSec,exa_regex=({time}\d{10})""",
    """exa_json_path=$..statusCode,exa_field_name=http_response_code""",
    """exa_json_path=$..queryStr,exa_field_name=query_string,exa_match_expr=!InList($.queryStr,"")""",
    """exa_json_path=$..UA,exa_field_name=user_agent,exa_match_expr=!InList($.UA,"")""",
    """exa_json_path=$..cliIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..reqPort,exa_field_name=dest_port""",
    """exa_json_path=$..reqHost,exa_field_name=web_domain""",
    """exa_json_path=$..reqMethod,exa_field_name=method""",
    """exa_json_path=$..reqPath,exa_field_name=uri_path""",
    """exa_json_path=$..reqQuery,exa_field_name=uri_query""",
    """exa_json_path=$..edgeIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$..bytes,exa_field_name=bytes""",
  ]


}
```