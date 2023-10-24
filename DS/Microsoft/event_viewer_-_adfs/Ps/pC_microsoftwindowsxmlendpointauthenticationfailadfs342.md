#### Parser Content
```Java
{
Name = "microsoft-windows-xml-endpoint-authentication-fail-adfs342"
  Vendor = "Microsoft"
  Product = "Event Viewer - ADFS"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
"""'AD FS'""",
"""<EventID>342</EventID>""",
"""Token validation failed"""
  ]
  Fields = [
"""SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)"""
"""<Computer>({host}[^\<]+)<\/Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<EventID>({event_code}[^\<]+)<\/EventID>"""
"""<EventRecordID>({event_id}[^\<]+)<\/EventRecordID>"""
"""ProcessID\\*='({process_id}[^\']+)"""
"""ThreadID\\*='({thread_id}[^\']+)"""
"""UserID\\*='({user_id}[^\']+)"""
"""<\/Data><Data>(({email_address}[^@<]+?@[^\.]+?\.[^-]+)|([^\s]+?))\s*\-({failure_reason}.+?)<\/Data><Data>"""
  ]
  ParserVersion = "v1.0.0"


}
```