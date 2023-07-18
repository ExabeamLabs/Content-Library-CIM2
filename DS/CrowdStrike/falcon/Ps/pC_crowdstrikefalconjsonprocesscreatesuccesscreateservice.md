#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-createservice
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
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
    """"event_platform":"({os}[^"]+)"""
  ]
  DupFields = [ "service_name->process_path_directory" ]  


}
```