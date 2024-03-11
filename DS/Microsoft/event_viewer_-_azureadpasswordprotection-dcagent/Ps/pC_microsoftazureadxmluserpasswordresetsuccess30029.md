#### Parser Content
```Java
{
Name = microsoft-azuread-xml-user-password-reset-success-30029
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>30029</EventID>""","""'Microsoft-AzureADPasswordProtection-DCAgent'""", """ UserName:""" ]
  Fields = ${MicrosoftParserTemplates.account-password-activity.Fields}[
      """<EventID>({event_code}30029)</EventID>"""
  ]
 
account-password-activity = {
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Message>({event_name}[^.<]+)""",
    """UserName:\s*({user}[^\s]+)""",
    """FullName:\s+({full_name}[^<]+?)\s+</Message>""",
    """Security UserID='({user_sid}[^']+)'""",
    """<Keywords>({action}[^<]+)</Keywords>""",
  
}
```