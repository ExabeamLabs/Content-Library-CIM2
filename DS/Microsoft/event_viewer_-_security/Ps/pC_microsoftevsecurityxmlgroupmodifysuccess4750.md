#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4750
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """<EventID>4750</EventID>""", """<Execution ProcessID""" , """<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Data Name =('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name =('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name =('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name =('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name =('|")TargetUserName('|")>({group_name}[^<]+)"""
    """<Data Name =('|")TargetDomainName('|")>({group_domain}[^<]+)<""",
    """<Data Name =('|")PrivilegeList('|")>(-|({privileges}[^<]+?))<""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """<Data Name =('|")TargetSid('|")>({group_id}[^<]+)""",
    """({event_code}4750)""",
    """<Level>({run_level}[^<]+)<"""
     ]
     DupFields = ["user->src_user", "domain->src_domain"]
  

}
```