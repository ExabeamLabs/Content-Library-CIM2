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
    """"(ServiceImagePath|CommandLine)":"(|({process_path}({process_dir}(?:(\w+:\\+)?[^:"]+?)?[\\\/])?({process_name}[^"\\\s]+?)))(\s|")""",
    """"ServiceDisplayName":"({service_name}[^"]+)""",
    """"UserName":"({user}[^"\s]+)"""",
    """"ServiceDescription":"({additional_info}[^"]+)"""
    """"aid":"({aid}[^"]+)""",	
    """"event_simpleName":"({event_code}CreateService)"""",
    """"ServiceImagePath":"({process_command_line}[^"]+)""",
    """"event_platform":"({os}[^"]+)"""
  ]
  DupFields = [ "service_name->process_path_directory" ]  


}
```