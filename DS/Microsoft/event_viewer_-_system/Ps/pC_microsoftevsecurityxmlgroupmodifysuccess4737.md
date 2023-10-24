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
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-]{1,40}\$?)</Data>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>({group_name}[^<]+)"""
    """<Data Name\\*=('|")TargetDomainName('|")>({group_domain}[^<]+)<""",
    """<Data Name\\*=('|")PrivilegeList('|")>(-|({privileges}[^<]+?))<""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
	  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
	  """<Data Name\\?='TargetSid'>({group_id}[^<]+)""",
	  """({event_name}A security-enabled global group was changed)""",
	  """({event_code}4737)"""
     ]
  

}
```