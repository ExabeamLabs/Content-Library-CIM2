#### Parser Content
```Java
{
Name = microsoft-evapp-xml-policy-apply-fail-4098
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """4098</EventID>""", """Group Policy Object did not apply""" ]
  Fields = [
    """({event_name}Group Policy Object did not apply)""",
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_code}4098)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Security UserID\\*='({user_sid}.+?)'\/>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """error code '({error_code}[^\s]+)\s"""
  ]


}
```