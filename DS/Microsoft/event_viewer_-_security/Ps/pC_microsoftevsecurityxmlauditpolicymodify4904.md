#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-audit-policy-modify-4904
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """An attempt was made to register a security event source""", """<EventID>4904<""" ]
  Fields = [
    """TimeCreated SystemTime(\\)?='({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """<Computer>({host}[^<]+)"""
    """<EventID>({event_code}\d+)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProcessId[^<>]+?>({process_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProcessName[^<>]+?>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>"""
    """({event_name}An attempt was made to register a security event source)"""
  ]
  DupFields = [ "host-> dest_host" ]


}
```