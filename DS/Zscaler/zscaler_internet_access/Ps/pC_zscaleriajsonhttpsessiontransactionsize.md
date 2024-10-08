#### Parser Content
```Java
{
Name = zscaler-ia-json-http-session-transactionsize
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"transactionsize":"""", """"threatcategory":"""", """"dlpengine":"""", """"url":"""", """"vendor":"Zscaler"""", """"product":"NSS"""", """"protocol":""", """"useragent":""" ]
  Fields = [
    """"datetime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"protocol":"({protocol}[^"]+)"""",
    """"action":"({action}[^"]+)"""",
    """"responsesize":"({bytes_in}\d+)"""",
    """"requestsize":"({bytes_out}\d+)"""",
    """"transactionsize":"({bytes}\d+)"""",
    """"urlsupercategory":"({category}[^"]+)""""
    """"urlcategory":"({category}[^"]+)"""",
    """"serverip":"({dest_ip}[a-fA-F\d:\.]+)"""",
    """"requestmethod":"(NA|({method}[^"]+))"""",
    """"refererURL":"(None|({referrer}[^"]+))"""",
    """"useragent":"(Unknown|({user_agent}[^"]+))"""",
    """"clientip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"status":"({result_code}\d{1,3})"""",
    """"user":"(({email_address}[^@"]+@[^\."]+\.[^"]+)|(AWS|([^"]+?->[^"]+)|({user}[\w\.\-]{1,40}\$?)))"""",
    """"url":"({url}(\w{1,5}:\/\/)?[^"\/\?]+({uri_path}\/[^"\?]*)?(\?({uri_query}[^"]*))?)"""",
    """"hostname":"(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^"]+))"""",
    """"appname":"({app}[^"]+)"""",
    """"reason":"(Allowed|({failure_reason}[^"]+))"""",
    """"devicehostname":"(NA|({src_host}[\w\.\-]+))""""
    """"location":"({location}[^",]+)""""
    """"department":"({department}[^",]+)""""
    """exa_json_path=$..datetime,exa_field_name=time""",
    """exa_json_path=$..protocol,exa_field_name=protocol""",
    """exa_json_path=$..action,exa_field_name=action""",
    """exa_json_path=$..responsesize,exa_field_name=bytes_in""",
    """exa_json_path=$..requestsize,exa_field_name=bytes_out""",
    """exa_json_path=$..transactionsize,exa_field_name=bytes""",
    """exa_json_path=$..urlsupercategory,exa_field_name=category""",
    """exa_json_path=$..urlcategory,exa_field_name=category""",
    """exa_json_path=$..serverip,exa_regex=({dest_ip}[a-fA-F\d:\.]+)""",
    """exa_json_path=$..requestmethod,exa_field_name=method,exa_match_expr=!InList(toLower($.[requestmethod]),"na")""",
    """exa_json_path=$..refererURL,exa_field_name=referrer,exa_match_expr=!InList(toLower($.[refererURL]),"none")""",
    """exa_json_path=$..useragent,exa_field_name=user_agent,exa_match_expr=!InList(toLower($.[useragent]),"unknown")""",
    """exa_json_path=$..ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$..status,exa_field_name=result_code""",
    """exa_json_path=$..user,exa_regex=(({email_address}[^@"]+@[^\."]+\.[^"]+)|(AWS|([^"]+?->[^"]+)|({user}[\w\.\-]{1,40}\$?)))"""
    """exa_json_path=$..url,exa_regex=({url}(\w{1,5}:\/\/)?[^"\/\?]+({uri_path}\/[^"\?]*)?(\?({uri_query}[^"]*))?)"""
    """exa_json_path=$..hostname,exa_regex=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^"]+))""",
    """exa_json_path=$..appname,exa_field_name=app""",
    """exa_json_path=$..reason,exa_field_name=failure_reason,exa_match_expr=!InList(toLower($.[reason]),"allowed")""",
    """exa_json_path=$..devicehostname,exa_regex=(NA|({src_host}[\w\.\-]+))"""
    """exa_json_path=$..location,exa_field_name=location""",
    """exa_json_path=$..department,exa_field_name=department"""
  ]
  DupFields = [ "result_code->http_response_code" ]


}
```