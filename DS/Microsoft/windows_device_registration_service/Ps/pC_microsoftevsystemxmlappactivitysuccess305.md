#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-app-activity-success-305
  Vendor = Microsoft
  Product = Windows Device registration service
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """<EventID>305<""", """Microsoft-Windows-User Device Registration""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,10}Z)'/>""",
    """<Execution ProcessID\\*='({process_id}\d+)'""",
    """<Security UserID\\*='({user_sid}\S+)'/>""",
    """<Computer>({host}[^"<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Message>({event_name}[^"\\\.]+)""",
    """<EventID>({event_code}305)</EventID>""",
    """<EventRecordID>({event_id}[^\<]+)<\/EventRecordID>"""
    """<Level>({run_level}[^<]+)<"""
   ]
   ParserVersion = "v1.0.0"


}
```