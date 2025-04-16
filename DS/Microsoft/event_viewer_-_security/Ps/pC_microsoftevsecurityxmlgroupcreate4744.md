#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-create-4744
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """<EventID>4744</EventID>""", """<Data Name ='TargetUserName'>""" ]
  Fields = [
    """<Computer>(::ffff:)?({dest_host}({host}[\w\-.]+))</Computer>""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)""",
    """<Keywords>({result_code}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Data Name ='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name ='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"""   
    """<Level>({run_level}[^<]+)<""",
    """<Data Name ='TargetDomainName'>({group_domain}[^<>]+?)</Data>""",
    """<Data Name ='TargetUserName'>({group_name}[^<>]+?)</Data>""",
    """<Data Name ='TargetSid'>({group_id}[^<>]+?)<\/Data>"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```