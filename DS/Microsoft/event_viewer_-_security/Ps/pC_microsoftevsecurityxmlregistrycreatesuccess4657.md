#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-registry-create-success-4657
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>4657</EventID>""", """<EventRecordID>""", ]
  Fields = [
    """<EventID>({event_code}\d+)</EventID>""",
    """<Keywords>({result}[^\<]+)</Keywords>""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<EventRecordID>({event_id}[^\<]+)</EventRecordID>""",
    """<Computer>({host}[^\<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^\<]+)</Data>""",
    """<Data Name\\*='SubjectUserName'>({user}[\w\.\-]{1,40}\$?)</Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^\<]+)</Data>""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^\<]+)</Data>""",
    """<Data Name\\*='HandleId'>({object_id}[^\<]+)</Data>""",
    """<Data Name\\*='OperationType'>({operation}[^\<]+)</Data>""",
    """<Data Name\\*='NewValueType'>(-|({registry_details_type}[^\<]+))</Data>""",
    """<Data Name\\*='NewValue'>(-|({registry_details}[^\<]+))</Data>""",
    """<Data Name\\*='ProcessId'>({process_id}[^\<]+)</Data>""",
    """<Data Name\\*='ProcessName'>({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))</Data>""",
    """<Data Name\\*='ObjectName'>({registry_key}[^\<]+)<\/Data>""",
    """<Data Name\\*='ObjectValueName'>({registry_value}[^\<]+)<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "host->src_host" ]


}
```