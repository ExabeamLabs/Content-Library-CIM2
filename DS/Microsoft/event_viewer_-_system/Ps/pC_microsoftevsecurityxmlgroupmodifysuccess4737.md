#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4737
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Security Group Management""", """<EventID>4737</EventID>""", """<Execution ProcessID""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Data Name ='SubjectUserName'>({user}[^<]+)</Data>""",
    """<Data Name ='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name ='TargetUserName'>({group_name}[^<]+)"""
    """<Data Name ='TargetDomainName'>({group_domain}[^<]+)<""",
    """<Data Name ='PrivilegeList'>({privileges}[^<]+?)<""",
    """<Execution ProcessID='({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
     ]
  

}
```