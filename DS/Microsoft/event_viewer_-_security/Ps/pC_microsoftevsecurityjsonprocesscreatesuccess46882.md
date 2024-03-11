#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-create-success-4688-2
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"event_id""", """4688""", """A new process has been created""" ]
    Fields = [
      """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s""",
      """"@timestamp"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
      """"Account"*:"*(({domain}[^"]+?)[\\\/]+)?({user}[^"\\\/]+)"""",
      """({event_code}4688)""",
      """"Activity"*:"*({event_name}[^"]+)""",
      """"hostname"*:"*({host}[^"]+)""",
      """"CommandLine"*:"*({process_command_line}[^"]+)""",
      """"NewProcessId"*:"*({process_guid}[^"]+)""",
      """"NewProcessName"*:"*({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
      """"SubjectLogonId"*:"*({login_id}[^"]+)""",
      """"SubjectUserName"*:"*(-|SYSTEM|({user}[^"]+?))""""
      """"SubjectDomainName"*:"*(-|({domain}[^"]+?))""""
    ]
    DupFields = [ "host->dest_host" ]
  

}
```