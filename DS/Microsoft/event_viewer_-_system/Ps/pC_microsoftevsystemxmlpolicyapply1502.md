#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-policy-apply-1502
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>1502<""", """<Provider Name""","""Microsoft-Windows-GroupPolicy""" ]
  Fields = [
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Security UserID\\*=('|")({user_sid}.+?)('|")\/>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Level>({run_level}[^<]+)"""
  ]


}
```