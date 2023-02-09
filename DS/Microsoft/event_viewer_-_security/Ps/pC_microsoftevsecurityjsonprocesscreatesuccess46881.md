#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-create-success-4688-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""","EventID":4688,""", 
"""A new process has been created"""
  ]
  Fields = [
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"""",
      """"Computer":"({host}[^"]+)"""",
      """"EventTime":({time}\d+)""",
      """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """"Account":"(({domain}[^"]+?)[\\\/]+)?({user}[^"\\\/]+)"""",
      """({event_code}4688)""",
      """({event_name}A new process has been created)""",
      """"Activity":"({event_name}[^"]+)""",
      """"Hostname":"({host}[^"]+)""",
      """"CommandLine":"\s*({process_command_line}[^"]+)""",
      """"NewProcessId":"({process_guid}[^"]+)""",
      """"NewProcessName":"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
      """"SubjectLogonId":"({login_id}[^"]+)""",
      """"SubjectUserName":"(-|SYSTEM|({user}[^"]+?))"""",
      """"SubjectDomainName":"(-|({domain}[^"]+?))""""
  ]
  DupFields = [ "host->dest_host" ]


}
```