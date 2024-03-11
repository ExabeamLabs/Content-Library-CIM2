#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-scheduled-task-modify-4702
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"EventID":4702""", """A scheduled task was updated""",""""TaskName":"""" ]
  Fields = [
    """"EventTime":\s*"?({time}[^",]+)""",
    """"Hostname":"({host}[\w.-]+?)"""",
    """"EventID":({event_code}\d+)""",
    """({event_name}A scheduled task was updated)""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"SubjectUserName":"({user}[^"]+)""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"TaskName":"({task_name}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"Keywords":"({result}[^,"]+)""",
    """<RunLevel>({run_level}[^<]+)<\/RunLevel>""",
    """<Command>({process_path}({process_dir}[^<]+)\\\\({process_name}[^<]+))<""",
    """<RegistrationInfo>[^=]+?<Description>(?=\w)({additional_info}[^=]+?)</Description>""",
  ]
  DupFields = [ "host->dest_host" ]


}
```