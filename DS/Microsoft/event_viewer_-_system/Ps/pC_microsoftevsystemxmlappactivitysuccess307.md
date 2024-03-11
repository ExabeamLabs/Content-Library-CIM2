#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-app-activity-success-307
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>307<""", """Automatic registration failed""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,10}Z)'/>""",
    """<Execution ProcessID='({process_id}\d+)'""",
    """<Computer>({host}[^"<]+)</Computer>""",
    """<Message>({event_name}[^"\\\.]+)""",
    """<Security UserID='({user_sid}\S+)'/>""",
    """<EventID>({event_code}307)</EventID>""",
    """<EventRecordID>({event_id}[^\<]+)<\/EventRecordID>"""
   ]
   ParserVersion = "v1.0.0"


}
```