#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-app-activity-success-304
  Vendor = Microsoft
  Product = Windows Device registration service
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = [ """<EventID>304<""", """Microsoft-Windows-User Device Registration""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,10}Z)'/>""",
    """<Execution ProcessID\\*='({process_id}\d+)'""",
    """<Computer>({host}[^"<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Message>({event_name}[^"\\\.]+)""",
    """<Security UserID\\*='({user_sid}\S+)'/>""",
    """<EventID>({event_code}304)</EventID>""",
    """<EventRecordID>({event_id}[^\<]+)<\/EventRecordID>"""
    """<Level>({run_level}[^<]+)<"""
   ]
   ParserVersion = "v1.0.0"


}
```