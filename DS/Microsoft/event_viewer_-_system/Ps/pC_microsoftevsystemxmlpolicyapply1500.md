#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-policy-apply-1500
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>1500</EventID>""", """The Group Policy settings for the computer were processed successfully""" ]
  Fields = [
    """({event_name}The Group Policy settings for the computer were processed successfully)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Security UserID\\*='({user_sid}.+?)'\/>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
# dc_name is removed
  ]


}
```