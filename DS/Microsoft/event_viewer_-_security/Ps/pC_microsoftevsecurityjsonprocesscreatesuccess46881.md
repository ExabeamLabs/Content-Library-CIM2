#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-create-success-4688-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
""","EventID":4688,""", 
"""A new process has been created"""
  ]
  Fields = [
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"Computer":"({host}[^"]+)"""",
      """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"Account":"(({domain}[^"]+?)[\\\/]+)?({user}[^"\\\/]+)"""",
      """({event_code}4688)""",
      """({event_name}A new process has been created)""",
      """"Activity":"({event_name}[^"]+)""",
      """"Hostname":"({host}[^"]+)""",
      """"CommandLine":"\s*({process_command_line}[^"]+)""",
      """"NewProcessId":"({process_guid}[^"]+)""",
      """"NewProcessName":"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
      """Creator Subject:.+?Account Name:\s*((\\)*(\\r|\\t|\\n))*(?:-|({user}[\w\.\-]{1,40}\$?))((\\)*(\\r|\\t|\\n))*\s*Account Domain:((\\)*(\\r|\\t|\\n))*\s*(?:-|({domain}.+?))((\\)*(\\r|\\t|\\n))*\s*Logon ID:((\\)*(\\r|\\t|\\n))*\s*({login_id}[^\\\s]+)"""
      """"SubjectLogonId":"({login_id}[^"]+)""",
      """"SubjectUserName":"(-|SYSTEM|({user}[^"]+?))"""",
      """"SubjectDomainName":"(-|({domain}[^"]+?))""""
      """"ComputerName":"({host}[^"]+)"""
      """"ParentProcessName":"({parent_process_path}({parent_process_dir}[^"]*?[\\\/]+)?({parent_process_name}[^"\\\/]+))""""
  ]
  DupFields = [ "host->dest_host" ]


}
```