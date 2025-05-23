#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-modify-fail-30002
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>30002</EventID>""", """<Provider Name""","""Microsoft-AzureADPasswordProtection-DCAgent""" ]
  Fields = ${WindowsParsersTemplates.account-password-activity.Fields}[
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}30002)</EventID>"""
  ]
  DupFields = [ "user->dest_user" ]

account-password-activity = {
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Message>({event_name}[^.<]+)""",
    """UserName:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """FullName:\s+({full_name}[^<]+?)\s+</Message>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Level>({run_level}[^<]+)<"""
  
}
```