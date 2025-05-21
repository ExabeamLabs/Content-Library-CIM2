#### Parser Content
```Java
{
Name = unix-unixnamed-json-dns-request-denied
  Conditions = [ """"message":"""", """ query (cache) """, """ denied """ ]
  Fields = ${BINDParserTemplates.bind-events.Fields} [
    """exa_json_path=$.message,exa_regex=client ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#|:)?({src_port}\d+)?\s+\((|({dns_query}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|([^\(\)]+))).*?\):\s*query \(cache\) \'({=query}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|([^\s\/']+))(\/({dns_query_type}[^\s\/']+)\/({dns_query_flags}[^\s\/']+))'""",
    """exa_regex=({action}denied)""",
  ]
  ParserVersion = "v1.0.0"

bind-events = {
  Vendor = Unix
  Product = Unix Named
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.priority,exa_field_name=priority""",
    """exa_json_path=$.beat.hostname,exa_field_name=host""",
    """exa_json_path=$.source,exa_field_name=log_source""",
    """exa_json_path=$.source,exa_regex=[^"]*?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(.log)(:({src_port}\d+))?""",
    """exa_json_path=$.message,exa_regex=[^"]*?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\#|:)?({src_port}\d+)?""",
    """exa_json_path=$.message,exa_field_name=additional_info""",
  
}
```