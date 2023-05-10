#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-handle-request-success-4659
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>4659</EventID>""", """Open Object with Delete Intent""", """NetApp-Security-Auditing""" ]
  Fields = [
    """TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}Open Object with Delete Intent)""",
    """<EventID>({event_code}4659)<\/EventID>""",
    """<Result>({action}[^<]+)<\/Result>""",
    """<Computer>([^\/]+\/)?({host}[^<]+)<\/Computer>""",
    """<Data Name ='SubjectIP'[^>]+>({src_ip}[A-Fa-f\d:.]+)<\/Data>""",
    """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<\/Data>""",
    """<Data Name ='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name ='SubjectUserName'>({user}[^<]+)<\/Data>""",
    """<Data Name ='ObjectServer'>({object_server}[^<]+)<\/Data>""",
    """<Data Name ='ObjectType'>({object_class}[^<]+)<\/Data>""",
    """<Data Name ='ObjectName'>({object}[^<]+)<\/Data>""",
    """<Data Name ='ObjectName'>({file_path}({file_dir}[^<]+)\/({file_name}[^<]+\.({file_ext}[^<]+)))<\/Data>""",
    """<Data Name ='DesiredAccess'>({access}[^<]+?)\s*<\/Data>""",
    """<Data Name ='HandleID'>({object_id}[^<]+)<\/Data>"""
  ]


}
```