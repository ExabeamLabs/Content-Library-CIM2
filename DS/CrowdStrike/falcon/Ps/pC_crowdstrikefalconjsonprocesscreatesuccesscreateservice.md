#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-createservice
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ 
""""event_simpleName":"CreateService"""" 
]
  Fields = [
    """"timestamp":\s*"*({time}\d{13})"""",
    """"ServiceImagePath":"(|({dest_process_path}({process_path}({dest_process_dir}({process_dir}(?:(\w+:\\+)?[^:"]+?))?[\\\/])?({dest_process_name}({process_name}[^"\\\s]+?)))))(\s|")""",
    """"ServiceDisplayName":"({service_name}[^"]+)""",
    """"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"ServiceDescription":"({additional_info}[^"]+)"""
    """"aid":"({aid}[^"]+)""",	
    """"event_simpleName":"({event_code}CreateService)"""",
    """"CommandLine":"({dest_process_command_line}({process_command_line}[^"]+))","""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"cid":"({cid}[^"]+)"""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.ServiceImagePath,exa_regex=(|({dest_process_path}({process_path}({dest_process_dir}({process_dir}(?:(\w+:\\+))?[^:"]+?)?[\\\/])?({dest_process_name}({process_name}[^"\\\s]+?)))))(\s|")""",
    """exa_json_path=$.ServiceDisplayName,exa_field_name=service_name"""
    """exa_regex="UserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """exa_json_path=$.ServiceDescription,exa_field_name=additional_info"""
    """exa_json_path=$.aid,exa_field_name=aid"""
    """exa_json_path=$.event_simpleName,exa_regex=({event_code}CreateService)"""
    """exa_json_path=$.CommandLine,exa_regex=({dest_process_command_line}({process_command_line}[^"]+))$""",
    """exa_json_path=$.event_platform,exa_field_name=os"""
    """exa_json_path=$.cid,exa_field_name=cid"""
  ] 


}
```