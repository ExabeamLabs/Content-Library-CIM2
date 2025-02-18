#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-modify-success-10024
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>10024</EventID>""", """<Provider Name""","""'Microsoft-AzureADPasswordProtection-DCAgent'""" ]
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,10}Z)'/>""",
    """<Data Name\\*='Data1'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name\\*='Data2'>({full_name}[^<]+)</Data>""",
    """<EventID>({event_code}10024)</EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Message>({additional_info}({event_name}[^<\.]+?)\.[^<]+?)\s+</Message>"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "user->dest_user" ]
  

}
```