#### Parser Content
```Java
{
Name = microsoft-evazureadppdca-xml-user-password-reset-fail-30005
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>30005</EventID>""", """<Provider Name ='Microsoft-AzureADPasswordProtection-DCAgent'""" ]
  Fields = ${DLWindowsParsersTemplates.account-password-reset.Fields}[
    """<EventID>({event_code}30005)</EventID>"""
  ]
  DupFields = [ "user->dest_user" ]

account-password-reset = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,10}Z)'/>""",
    """<Message>({event_name}[^.<]+)""",
    """UserName:\s*({user}[^\s]+)""",
    """FullName:\s+({full_name}[^<]+?)\s+</Message>""",
    """Security UserID='({user_sid}[^']+)'""",
    """<Keywords>({result}[^<]+)</Keywords>""",
  
}
```