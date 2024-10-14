#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-20001
  ParserVersion = "v1.0.0"
  Product = "Event Viewer - AzureADPasswordProtection-DCAgent"
  Conditions = [ """<EventID>20001</EventID>""",  """<Computer>""" ,"""<Channel>Microsoft-AzureADPasswordProtection-DCAgent/Operational</Channel>""" ]
  Fields = ${DLWindowsParsersTemplates.azure-ad-system-info.Fields}[
    """<EventID>({event_code}20001)</EventID>"""
  ]
 
azure-ad-system-info = {
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Message>({event_name}[^<\.:]+?)(<|\.|:)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```