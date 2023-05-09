#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-service-state-modify-4
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4</EventID>""", """<Message>Sysmon service state changed:""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """({event_name}Sysmon service state changed)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Security UserID\\*='({user_sid}.+?)'\/>""",
    """<Data Name\\*='State'>({state}.+?)<\/Data>""",
    """({log_name}Microsoft-Windows-Sysmon)""",
  ]


}
```