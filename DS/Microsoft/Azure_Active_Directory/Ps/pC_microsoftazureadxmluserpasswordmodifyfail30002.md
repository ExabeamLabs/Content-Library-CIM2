#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-modify-fail-30002
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>30002</EventID>""", """<Provider Name ='Microsoft-AzureADPasswordProtection-DCAgent'""" ]
  Fields = ${WindowsParsersTemplates.account-password-activity.Fields}[
    """<EventID>({event_code}30002)</EventID>"""
  ]
  DupFields = [ "user->dest_user" ]

account-password-activity = {
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Message>({event_name}[^.<]+)""",
    """UserName:\s*({user}[^\s]+)""",
    """FullName:\s+({full_name}[^<]+?)\s+</Message>""",
    """Security UserID='({user_sid}[^']+)'""",
    """<Keywords>({result}[^<]+)</Keywords>""",
  
}
```