#### Parser Content
```Java
{
Name = "apache-a-json-http-session-chcomaccesslog"
Vendor = "Apache"
Product = "Apache"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
"""chcom_access_log"""
"""apache_access_log"""
""""request":""""
""""response":""""
]
Fields = [
"""exa_json_path=$.@timestamp,exa_field_name=time"""
"""exa_json_path=$.host.name,exa_field_name=host"""
"""exa_json_path=$.remote_addr,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.verb,exa_field_name=method"""
"""exa_json_path=$.request,exa_regex=({uri_path}[^"\?\s]+)(?:\?({uri_query}[^?\s"]+))?"""
"""exa_json_path=$.response,exa_field_name=http_response_code"""
"""exa_json_path=$.bytes,exa_field_name=bytes_out"""
"""exa_json_path=$.referrer,exa_field_name=referrer"""
"""exa_json_path=$.user_agent,exa_field_name=user_agent"""
"""exa_json_path=$.location,exa_field_name=url"""
]
ParserVersion = "v1.0.0"


}
```