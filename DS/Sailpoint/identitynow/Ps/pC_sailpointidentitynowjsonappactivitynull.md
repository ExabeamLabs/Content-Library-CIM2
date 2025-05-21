#### Parser Content
```Java
{
Name = sailpoint-identitynow-json-app-activity-null
  ExtractionType = json
  Conditions = [""""type": null""", """"application":""", """"id":"""]
  Fields = ${SailPointParserTemplates.s-sailpoint-activity.Fields} [
    """exa_json_path=$.application,exa_regex=((?i:null|NONE)|({app}[^"]+))""",
    """exa_json_path=$.info,exa_regex=((?i:null|NONE)|({additional_info}[^"]+))"""
  ]
  ParserVersion = "v1.0.0"

s-sailpoint-activity = {
  Vendor = Sailpoint
  Product = IdentityNow
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"hostname":\s*"((\d)|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(\d+)|({src_host}[^"]+))"""",
    """"datetime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """"action":\s*"({operation}[^"]+)",""",
    """"ipaddr":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"target":\s*"((\d+)|(unknown|Not Available)|(({last_name}[^,"]+),\s*({first_name}[^"]+)))"""",
    """"source":\s*"((\d+)|(unknown|Not Available)|(({last_name}[^,"]+),\s*({first_name}[^"]+)))"""",
    """"target":\s*"((unknown|Not Available)|({full_name}[^\s",]+\s+[^"]+))"""",
    """"source":\s*"((unknown|Not Available)|({full_name}[^\s",]+\s+[^"]+))"""",
    """"target":\s*"((unknown|Not Available)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"source":\s*"((unknown|Not Available)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"id":\s*"({fingerprint}[^"]+)",""",
    """"type":\s*"((NONE)|({event_subtype}[^"]+))""""

    """exa_json_path=$.hostname,exa_regex=((\d)|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(\d+)|({src_host}[^"]+))$""",
    """exa_json_path=$.datetime,exa_field_name=time""",
    """exa_json_path=$.action,exa_field_name=operation""",
    """exa_json_path=$.ipaddr,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.target,exa_regex=((\d+)|(?i:null|unknown|Not Available)|({full_name}({last_name}[^,"]+),\s*({first_name}[^"]+)))""",
    """exa_json_path=$.source,exa_regex=((\d+)|(?i:null|unknown|Not Available)|({full_name}({last_name}[^,"]+),\s*({first_name}[^"]+)))""",
    """exa_json_path=$.target,exa_regex=^((?i:null|unknown|Not Available)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$.source,exa_regex=^((?i:null|unknown|Not Available)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$.id,exa_field_name=fingerprint""",
    """exa_json_path=$.type,exa_regex=((?i:NONE|null)|({event_subtype}[^"]+))"""
  
}
```