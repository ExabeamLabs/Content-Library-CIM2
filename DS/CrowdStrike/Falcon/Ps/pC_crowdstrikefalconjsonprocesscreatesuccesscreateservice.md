#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-createservice
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""event_simpleName":"CreateService"""" 
]
  Fields = [
    """"timestamp":"({time}\d{10})"""",
    """"(ServiceImagePath|CommandLine)":"(|({process_path}({process_dir}(?:(\w+:\\+)?[^:"]+?)?[\\\/])?({process_name}[^"\\\s]+?)))(\s|")""",
    """"ServiceDisplayName":"({service_name}[^"]+)""",
    """"UserName":"({user}[^"\s]+)"""",
    """"ServiceDescription":"({additional_info}[^"]+)"""
    """"aid":"({aid}[^"]+)""",	
    """"event_simpleName":"({event_code}CreateService)"""",
    """"ServiceImagePath":"({process_command_line}[^"]+)"""
  ]
  DupFields = [ "service_name->process_path_directory" ]  


}
```