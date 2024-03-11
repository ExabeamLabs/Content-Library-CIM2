#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-reset-success-10015
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>10015</EventID>""", """Microsoft-AzureADPasswordProtection-DCAgent""", """ UserName:""", """The reset password for the specified user was validated as compliant with the current Azure password policy""" ]
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Data Name ='Data1'>({user}[^<]+)</Data>""",
    """<Data Name ='Data2'>({full_name}[^<]+)</Data>""",
    """<EventID>({event_code}10015)</EventID>""",
    """({event_name}The reset password for the specified user was validated as compliant with the current Azure password policy)"""
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID='({user_sid}[^']+)'""",
    """<Message>({additional_info}[^<]+?)\s+</Message>"""
  ]


}
```