#### Parser Content
```Java
{
Name = microsoft-evazureadppdca-xml-endpoint-activity-fail-30036
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>30036</EventID>""", """Microsoft-AzureADPasswordProtection-DCAgent""", """<Computer>""" ]
  Fields = ${DLWindowsParsersTemplates.azure-ad-system-info.Fields}[
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}30036)</EventID>"""
  ]

azure-ad-system-info = {
  Vendor = Microsoft
  Product = Azure Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """Security UserID\\*='({user_sid}[^']+)'""",
    """<Message>({event_name}[^<\.:]+?)(<|\.|:)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```