#### Parser Content
```Java
{
Name = microsoft-evazureadppdca-xml-endpoint-activity-fail-30044
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>30044</EventID>""", """Microsoft-AzureADPasswordProtection-DCAgent""", """<Computer>""" ]
  Fields = ${DLWindowsParsersTemplates.azure-ad-system-info.Fields}[
    """<EventID>({event_code}30044)</EventID>"""
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