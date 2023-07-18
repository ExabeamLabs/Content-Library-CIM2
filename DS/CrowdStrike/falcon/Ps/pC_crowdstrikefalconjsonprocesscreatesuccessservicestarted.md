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
    """"UserName":\s*"((LOCAL SERVICE|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))))"""",
    """"UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\-\.]+\$?))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """"ImageFileName":\s*"[\\\?]+(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))""""
    """"aid":\s*"({aid}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)"""
    """"InterfaceGuid":"({process_guid}[^"]+)""""
  ]
  DupFields = [ "process_dir->process_path_directory", "process_command_line->parent_process_command_line" ]


}
```