#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-audit-policy-modify-4905
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """An attempt was made to unregister a security event source""", """<EventID>4905<""" ]
  Fields = [
    """TimeCreated SystemTime(\\)?='({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """<Computer>({host}[^<]+)"""
    """<EventID>({event_code}\d+)""",
    """({event_name}An attempt was made to unregister a security event source)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
# src_name is removed
# src_id is removed
    """<Data Name[^<>]+?ProcessId[^<>]+?>({process_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProcessName[^<>]+?>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>""",
  ]
  DupFields = [ "host-> dest_host" ]


}
```