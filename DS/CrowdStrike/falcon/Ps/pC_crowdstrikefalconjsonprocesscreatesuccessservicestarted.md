#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-servicestarted
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Conditions = [ 
""""event_simpleName":""""
"""ServiceStarted""" 
]
  Fields = [
    """"timestamp":\s*"({time}\d{13})"""",
    """"CommandLine":\s*"({process_command_line}.+?)\s*","TargetProcessId""",
    """"name":\s*"({service_name}[^"]+)""",
    """"ServiceDisplayName":"({service_name}[^"]+)"""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"UserName":\s*"((LOCAL SERVICE|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+)))|({user}[^"\s]+))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """"ImageFileName":\s*"[\\\?]+(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))""""
    """"aid":\s*"({aid}[^"]+)"""
  ]
  DupFields = [ "process_dir->process_path_directory" ]


}
```