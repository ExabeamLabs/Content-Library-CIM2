#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-password-read-5379-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Product = Event Viewer - Security
  Conditions = [ """<EventID>5379<""", """User Account Management""", """<Provider Name""","""Microsoft-Windows-Security-Auditing"""]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<""",
    """Guid\\*=('|")\{({process_guid}[^\'\"\}]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<EventID[^<]*?>({event_code}\d+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*=('|")({provider_name}[^\'\"]+)""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name\\*=('|")ReadOperation('|")>({additional_info}[^<]+?)</Data>"""
 ]


}
```