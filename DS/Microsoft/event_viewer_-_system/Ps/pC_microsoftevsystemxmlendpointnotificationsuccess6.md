#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-6
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>6</EventID>""", """<EventRecordID>""", """Microsoft-Windows-FilterManager""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Computer>({dest_host}({host}[\w\-.]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Security UserID\\*=('|")({user_sid}.+?)'\/>""",
    """<Level>({run_level}\d+)"""
    """><Data Name =("|')ExtraInfoString("|')>({additional_info}[^<]+?)\s*<"""
    """Guid=('|")\{({process_guid}[^"'\}]+)"""
    """<Provider>({provider_name}[^<]+?)</Provider>""",
    """ThreadID\\*='({thread_id}[^']+)""",
  ]
  


}
```