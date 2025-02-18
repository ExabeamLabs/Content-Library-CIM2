#### Parser Content
```Java
{
Name = microsoft-evazureadppdca-xml-app-authentication-success-30030
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>30030</EventID>""", """Microsoft-AzureADPasswordProtection-DCAgent""", """<Computer>"""]
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<EventID>({event_code}30030)</EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Message>({event_name}[^<\.:]+?)(<|\.|:)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```