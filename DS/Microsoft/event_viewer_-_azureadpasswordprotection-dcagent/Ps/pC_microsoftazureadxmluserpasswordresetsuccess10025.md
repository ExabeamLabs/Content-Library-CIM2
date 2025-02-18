#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-reset-success-10025
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>10025</EventID>""", """<Provider Name""","""'Microsoft-AzureADPasswordProtection-DCAgent'""" ]
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Data Name\\*='Data1'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name\\*='Data2'>({full_name}[^<]+)</Data>""",
    """<EventID>({event_code}10025)</EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Message>({additional_info}({event_name}[^<\.]+?)\.[^<]+?)\s+</Message>"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "user->dest_user" ]


}
```