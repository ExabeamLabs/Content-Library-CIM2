#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-scheduled-task-modify-4702
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """4702""", """A scheduled task was updated""","""Task Name:""", """CEF:""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"(?:winlog\.)?computer_name":"({host}[^"]+)"""",
    """"event_id":({event_code}\d+)""",
    """"message":"({event_name}[^=]+?)\.?\\[nt]""",
    """"outcome":"({result}[^"]+)"""",
    """"user":(\{[^=]*?"name":"({user}[^"]+)|"({=user}[^"]+))""",
    """"user":\{[^=]*?"id":"({user_sid}[^"]+)"""",
    """"user":\{[^=]*?"domain":"({domain}[^"]+)"""",
    """"TaskName":"({task_name}[^"]+)"""",
    """<RunLevel>({run_level}[^<]+)<\/RunLevel>""",
    """<Command>({process_path}({process_dir}[^<]+)\\\\({process_name}[^<]+))<""",
    """<RegistrationInfo>[^=]+?<Description>(?=\w)({additional_info}[^=]+?)</Description>""",
    """"logon":\{"id":"({login_id}[^"]+)"""",
  ]
  DupFields = [ "host->dest_host" ]


}
```