#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-create-success-4688
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
""","EventID":"4688",""",
"""A new process has been created"""
   ]
    Fields = [
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"Account":"(({domain}[^"]+?)[\\\/]+)?({user}[^"\\\/]+)"""",
      """({event_code}4688)""",
      """"Activity":"({event_name}[^"]+)""",
      """"Computer":"({host}[^"]+)""",
      """"CommandLine":"({process_command_line}[^"]+)""",
      """"NewProcessId":"({process_guid}[^"]+)""",
      """"NewProcessName":"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
      """"SubjectLogonId":"({login_id}[^"]+)""",
    ]
    DupFields = [ "host->dest_host" ]
  

}
```