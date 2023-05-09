#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-log-clear-success-1102-1
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [  """>1102</EventID>""", """<TimeCreated SystemTime"""    ]
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
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
    """Account Name:\s*(LOCAL SERVICE|-|({user}\S+))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+""",
    """Client IP: ({src_ip}[a-fA-F:\.\d]+)""",
    """ThreadID(\\)?='({thread_id}\d+)"""
  ]


}
```