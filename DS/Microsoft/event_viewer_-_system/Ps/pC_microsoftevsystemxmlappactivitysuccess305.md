#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-app-activity-success-305
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>305<""", """Automatic registration failed at authentication phase""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,10}Z)'/>""",
    """<Execution ProcessID\\*='({process_id}\d+)'""",
    """<Security UserID\\*='({user_sid}\S+)'/>""",
    """<Computer>({host}[^"<]+)</Computer>""",
    """<Message>({event_name}[^"\\\.]+)""",
    """<EventID>({event_code}305)</EventID>""",
    """<EventRecordID>({event_id}[^\<]+)<\/EventRecordID>"""
   ]
   ParserVersion = "v1.0.0"


}
```