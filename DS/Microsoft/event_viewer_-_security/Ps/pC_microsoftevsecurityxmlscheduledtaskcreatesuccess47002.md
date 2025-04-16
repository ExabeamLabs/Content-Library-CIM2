#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4700-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """<EventID>4700</EventID>""", """<Provider Name""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """Guid\\*=('|")\{({process_guid}[^\"'\}]+)""",
    """({event_code}4700)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*=('|")({provider_name}[^\"']+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^"']+)""",
    """<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name =('|")TaskName('|")>({task_name}[^<]+)"""
    """<Data Name =('|")TaskContent('|")>({additional_info}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host-> dest_host", "user->src_user", "domain->src_domain"]


}
```