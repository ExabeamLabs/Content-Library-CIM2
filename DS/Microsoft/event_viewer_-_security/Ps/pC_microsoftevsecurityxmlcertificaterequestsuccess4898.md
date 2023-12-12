#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-certificate-request-success-4898
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4898</EventID>""", """<Message>Certificate Services loaded a template""", """'Microsoft-Windows-Security-Auditing'""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)'""",
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'\/>""",
    """<Data Name\\*='Requester'>(({domain}[^<\\]+)\\)?({user}[\w\.\-]{1,40}\$?)<""",
    """<Data Name\\*='Attributes'>\s*({attributes}[^<]+?)\s*<""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({sub_category}[^<]+)"""
  ]


}
```