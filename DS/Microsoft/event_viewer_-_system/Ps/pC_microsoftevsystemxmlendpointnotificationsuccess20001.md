#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-20001
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  Conditions = [ """<EventID>20001</EventID>""", """Microsoft-AzureADPasswordProtection-DCAgent""", """<Computer>""" ]
  Fields = ${DLWindowsParsersTemplates.azure-ad-system-info.Fields}[
    """<EventID>({event_code}20001)</EventID>"""
  ]
 
azure-ad-system-info = {
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)'/>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID='({user_sid}[^']+)'""",
    """<Message>({event_name}[^<\.:]+?)(<|\.|:)"""
  
}
```