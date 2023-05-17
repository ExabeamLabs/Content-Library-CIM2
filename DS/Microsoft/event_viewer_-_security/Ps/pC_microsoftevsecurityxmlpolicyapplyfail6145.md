#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-policy-apply-fail-6145
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>6145</EventID>""", """<Message>One or more errors occured while processing security policy in the group policy objects""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}One or more errors occured while processing security policy in the group policy objects)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)' ThreadID\\*='({thread_id}\d+)'""",
    """<EventRecordID>({event_id}\d+)""",
    """<Data Name\\*='ErrorCode'>({error_code}\d+)<\/Data>""",
    """<Keywords>({action}[^<]+)<\/Keywords>""",
    """<Opcode>({severity}[^<]+)<\/Opcode>""",
    """<Message>\s*({additional_info}[^<]+?)\s*<\/Message>""",
  ]


}
```