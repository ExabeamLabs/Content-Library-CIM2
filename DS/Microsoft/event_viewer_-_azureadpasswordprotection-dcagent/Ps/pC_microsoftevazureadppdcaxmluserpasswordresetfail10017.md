#### Parser Content
```Java
{
Name = microsoft-evazureadppdca-xml-user-password-reset-fail-10017
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>10017</EventID>""", """<Provider Name""","""'Microsoft-AzureADPasswordProtection-DCAgent'""" ]
  Fields = ${DLWindowsParsersTemplates.account-password-reset.Fields}[
    """<EventID>({event_code}10017)</EventID>"""
  ]
  DupFields = [ "user->dest_user" ]

account-password-reset = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,10}Z)'/>""",
    """<Message>({event_name}[^.<]+)""",
    """UserName:\s*({user}[\w\.\-]{1,40}\$?)""",
    """FullName:\s+({full_name}[^<]+?)\s+</Message>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Keywords>({result}[^<]+)</Keywords>""",
  
}
```