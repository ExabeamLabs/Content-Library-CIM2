#### Parser Content
```Java
{
Name = microsoft-evazureadppdca-xml-endpoint-notification-success-30042
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>30042</EventID>""", """Microsoft-AzureADPasswordProtection-DCAgent""", """<Computer>""" ]
  Fields = ${DLWindowsParsersTemplates.azure-ad-system-info.Fields}[
    """<EventID>({event_code}30042)</EventID>"""
  ]

azure-ad-system-info = {
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Message>({event_name}[^<\.:]+?)(<|\.|:)"""
  
}
```