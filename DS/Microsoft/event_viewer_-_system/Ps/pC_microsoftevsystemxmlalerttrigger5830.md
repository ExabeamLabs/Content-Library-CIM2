#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-alert-trigger-5830
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """>5830</EventID>""", """NETLOGON""", """<EventData><Data>""" ]
  Fields = [
    """<Computer>({host}[^<\.]+)\.({domain}[^<]+)<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime\\*=(?:["']+)?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID[^>]+>({event_code}\d+)<""",
    """<Provider Name\\*=(?:["']+)?({provider_name}[\w-]+)""",
    """<Level>({alert_severity}\d+)""",
    """<Keywords>({result}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)""",
    """<EventData><Data>([^<]+)<\/Data><Data>({domain}[^<]+?)\.*<\/Data><Data>({user_type}[^<]+)<\/Data><Data>({os}[^<]+)<\/Data><Data>([^<]+)<\/Data><Data>(?:(?i)N\/A|([^<]+))<"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```