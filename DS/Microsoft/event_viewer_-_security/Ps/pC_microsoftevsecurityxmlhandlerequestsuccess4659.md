#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-handle-request-success-4659
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>4659</EventID>""", """<EventName>Open Object with Delete Intent""", """NetApp-Security-Auditing""" ]
  Fields = [
    """TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}Open Object with Delete Intent)""",
    """<EventID>({event_code}4659)<\/EventID>""",
    """<Result>({action}[^<]+)<\/Result>""",
    """<Computer>([^\/]+\/)?({host}[^<]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name\\*='SubjectIP'[^>]+>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/Data>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>""",
    """<Data Name\\*='ObjectServer'>({object_server}[^<]+)<\/Data>""",
    """<Data Name\\*='ObjectType'>({object_class}[^<]+)<\/Data>""",
    """<Data Name\\*='ObjectName'>({object}[^<]+)<\/Data>""",
    """<Data Name\\*='ObjectName'>({file_path}({file_dir}[^<]+)\/({file_name}[^<]+\.({file_ext}[^<]+)))<\/Data>""",
    """<Data Name\\*='DesiredAccess'>({access}[^<]+?)\s*<\/Data>""",
    """<Data Name\\*='HandleID'>({object_id}[^<]+)<\/Data>""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```