#### Parser Content
```Java
{
Name = microsoft-evapp-xml-log-clear-success-1102
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = Event Viewer - Application
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [  """<EventID>1102</EventID>""", """<TimeCreated SystemTime""","""<Channel>Application</Channel>"""    ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Computer>({host}({dest_host}[\w\-.]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Message>({event_name}[^:<\.]+)""",
    """<Message>({event_name}[^<]+?)\.(\s|<)""",
    """<Message>({additional_info}[^<]+)\s*<\/Message>""",
    """<Message>Process '?({process_name}[^\s']+)""",
    """<Security UserID(\\)?='({user_sid}[^']+)""",
    """<Execution ProcessID(\\)?='({process_id}[^']+)""",
    """<EventID[^<]*?>({event_code}\d+)""",
    """<Keyword>(Classic|({result}[^<]+))</Keyword>""",
    """<Data Name(\\)?='ProcessName'>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>""",
    """<Data Name\\*='TargetProcessName'>({dest_process_path}({dest_process_dir}[^<>]*?[\\\/]+)?({dest_process_name}[^<>\\\/]+))</Data>""",
    """<Data Name(\\)?='ProcessId'>({process_id}[^<]+?)\s*</Data>""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+""",
    """Client IP: ({src_ip}[a-fA-F:\.\d]+)""",
    """ThreadID(\\)?='({thread_id}\d+)""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```