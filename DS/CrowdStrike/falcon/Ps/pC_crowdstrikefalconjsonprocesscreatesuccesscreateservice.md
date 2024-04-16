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
    """"ServiceImagePath":"(|({process_path}({process_dir}(?:(\w+:\\+)?[^:"]+?)?[\\\/])?({process_name}[^"\\\s]+?)))(\s|")""",
    """"ServiceDisplayName":"({service_name}[^"]+)""",
    """"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""",
    """"ServiceDescription":"({additional_info}[^"]+)"""
    """"aid":"({aid}[^"]+)""",	
    """"event_simpleName":"({event_code}CreateService)"""",
    """"CommandLine":"({process_command_line}[^"]+)","""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"cid":"({cid}[^"]+)"""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.ServiceImagePath,exa_regex=(|({process_path}({process_dir}(?:(\w+:\\+)?[^:"]+?)?[\\\/])?({process_name}[^"\\\s]+?)))(\s|")""",
    """exa_json_path=$.ServiceDisplayName,exa_field_name=service_name"""
    """exa_regex="UserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""",
    """exa_json_path=$.ServiceDescription,exa_field_name=additional_info"""
    """exa_json_path=$.aid,exa_field_name=aid"""
    """exa_json_path=$.event_simpleName,exa_regex=({event_code}CreateService)"""
    """exa_json_path=$.CommandLine,exa_regex=({process_command_line}[^"]+)","""",
    """exa_json_path=$.event_platform,exa_field_name=os"""
    """exa_json_path=$.cid,exa_field_name=cid"""
  ]
  DupFields = [ "service_name->process_path_directory", "process_path->dest_process_path","process_dir->dest_process_dir","process_name->dest_process_name","process_command_line->dest_process_command_line" ]  


}
```