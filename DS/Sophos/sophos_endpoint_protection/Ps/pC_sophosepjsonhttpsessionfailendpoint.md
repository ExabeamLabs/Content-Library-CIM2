#### Parser Content
```Java
{
Name = "sophos-ep-json-http-session-fail-endpoint"
ExtractionType = json
ParserVersion = "v1.0.0"
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""Event::Endpoint::Web"""
]
Fields = [

    """exa_json_path=$.location,exa_field_name=host""",
    """exa_json_path=$.when,exa_field_name=time""",
    """exa_json_path=$.rt,exa_field_name=time""",
    """exa_json_path=$.name,exa_regex=(n\/a|({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\'))""",
    """exa_json_path=$.name,exa_regex='({target}[^']+)'\s+({alert_name}[^"']+)\s""",
    """exa_json_path=$.name,exa_regex=({alert_name}[^"']+)\sto '({target}[^']+)'\s+""",
    """exa_json_path=$.name,exa_regex='({malware_url}[^"\'\s]+)'\s+blocked due to""",
    """exa_json_path=$.name,exa_regex=[^"]*?block to\s+'({malware_url}[^"\'\s]+)'""",
    """exa_json_path=$.name,exa_regex=(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """exa_json_path=$.name,exa_field_name=additional_info""",
    """exa_json_path=$.type,exa_field_name=alert_type""",
    """exa_json_path=$.dhost,exa_field_name=src_host""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.suser,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-]{1,40}\$?)))$""",
    """exa_json_path=$.source,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-]{1,40}\$?)))$""",
    """exa_json_path=$.source,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.id,exa_field_name=alert_id"""
   ]


}
```