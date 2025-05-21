#### Parser Content
```Java
{
Name = zscaler-ia-json-http-session-transactionsize-1
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Conditions = [ """"transaction_size":"""", """"threat_category":"""", """"dlp_engine":"""", """"url":"""", """"vendor":"Zscaler"""", """"product":"NSS"""", """"protocol":""", """"user_agent":""" ]
  Fields = [
    """exa_json_path=$.datetime,exa_field_name=time""",
    """exa_json_path=$.protocol,exa_field_name=protocol""",
    """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.bytes_in,exa_field_name=bytes_in""",
    """exa_json_path=$.bytes_out,exa_field_name=bytes_out""",
    """exa_json_path=$.transaction_size,exa_field_name=bytes""",
    """exa_json_path=$.url_super_category,exa_field_name=category""",
    """exa_json_path=$.url_category,exa_field_name=category""",
    """exa_json_path=$.dest_ip,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$.request_method,exa_field_name=method,exa_match_expr=!InList(toLower($.[requestmethod]),"na")""",
    """exa_json_path=$.referer,exa_field_name=referrer,exa_match_expr=!InList(toLower($.[refererURL]),"none")""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent,exa_match_expr=!InList(toLower($.[useragent]),"unknown")""",
    """exa_json_path=$.src_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$.user,exa_regex=^(({email_address}[^@"]+@[^\."]+\.[^"]+)|(AWS|([^"]+?->[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
    """exa_json_path=$.url,exa_regex=^({url}(\w{1,5}:\/\/)?[^"\/\?]+({uri_path}\/[^"\?]*)?(\?({uri_query}[^"]*))?)$""",
    """exa_json_path=$.hostname,exa_regex=^(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^"]+))$""",
    """exa_json_path=$.app_name,exa_field_name=app""",
    """exa_json_path=$.reason,exa_field_name=failure_reason,exa_match_expr=!InList(toLower($.[reason]),"allowed")""",
    """exa_json_path=$.device_hostname,exa_regex=^(NA|({src_host}[\w\.\-]+))$""",
    """exa_json_path=$.location,exa_field_name=location""",
    """exa_json_path=$.department,exa_field_name=department""",
    """exa_json_path=$.src_translated_ip,exa_regex=^({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$.os,exa_field_name=os"""
  ]
  ParserVersion = "v1.0.0"


}
```