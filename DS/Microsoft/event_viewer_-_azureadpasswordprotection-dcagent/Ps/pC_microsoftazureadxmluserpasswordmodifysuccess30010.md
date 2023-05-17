#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-modify-success-30010
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>30010</EventID>""", """'Microsoft-AzureADPasswordProtection-DCAgent'""", """ UserName:""" ]
  Fields = [
    """<EventID>({event_code}30010)</EventID>"""
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Message>({event_name}[^.<]+)""",
    """UserName:\s*({user}[^\s]+)""",
    """FullName:\s+({full_name}[^<]+?)\s+</Message>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Keywords>({result}[^<]+)</Keywords>""",
  ]


}
```