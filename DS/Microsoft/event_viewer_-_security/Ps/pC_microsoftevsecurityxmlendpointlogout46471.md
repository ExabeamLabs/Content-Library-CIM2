#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-logout-4647-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4647</EventID>""", """<Task>Logoff""", """<Provider Name""","""Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'\}"]+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<Data Name\\*=('|")TargetDomainName('|")>({dest_domain}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>({dest_user}[^<]+)<\/Data>"""
   ]


}
```