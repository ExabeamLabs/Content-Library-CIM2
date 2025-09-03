#### Parser Content
```Java
{
Name = sophos-ep-cef-app-notification-registered
  ParserVersion = v1.0.0
  Product = Sophos Endpoint Protection
  Conditions = [ """"endpoint_id":""", """"Event::Endpoint::Registered""", """"endpoint_type":""" ]

sophos-events-aa = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"location":"({host}[^"]+)""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({event_name}[^"]+)""",
    """"type":\s*"({event_category}[^"]+)""",
    """"dhost":\s*"({dest_host}[\w\-.]+)"""",
    """"severity":\s*"({severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"suser":\s*"(n\/a|({full_name}[^"\\\s,]+\s+[^"\\,]+))"""",
    """"suser":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
# id is removed
    """"source":"(?:n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\\"source_info\\"__ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source_info":\s*\{"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source":"(({domain}[^\\",]+?)\\+)?(?:n\/a|Administrator|({full_name}(?:({first_name}[^\s",.\\]+)(?:\s+|\.))({last_name}[^",\\]+)))"""",
    """"source":"((({domain}[^\",]+?)\\+)?(?:n/a|Administrator|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """destinationServiceName =({app}[^=]+)\s+\w+="""

    """exa_json_path=$.location,exa_field_name=host""",
    """exa_json_path=$.when,exa_field_name=time""",
    """exa_json_path=$.rt,exa_field_name=time""",
    """exa_json_path=$.name,exa_regex=({event_name}[^"':]+)""",
    """exa_json_path=$.type,exa_field_name=event_category""",
    """exa_json_path=$.dhost,exa_field_name=dest_host""",
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.suser,exa_regex=(?:n\/a|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
    """exa_json_path=$.source_info.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.source,exa_regex=(?:n\/a|Administrator|((({domain}[^\\"]+)\\+)?({full_name}({last_name}[^\\\(\)\s",]+),?\s+({first_name}[^\\\(\)",]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|((({=domain}[^\\",]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))$"""
  ]
  DupFields = [ "host->src_host" 
}
```