#### Parser Content
```Java
{
Name = microsoft-evazureadppdca-xml-app-notification-30006
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - AzureADPasswordProtection-DCAgent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = ["""The service is now enforcing the following Azure password policy""","""<EventID>30006</EventID>""","""Microsoft-AzureADPasswordProtection-DCAgent"""]
  Fields = [
     """<TimeCreated\sSystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
         """<Computer>({host}[^<]+)<\/Computer>""",
         """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
         """<EventID>({event_code}[^<]+)<\/EventID>""",
         """({event_name}The service is now enforcing the following Azure password policy)""",
         """<Security\sUserID\\*='({user_sid}[^']+)'""",
         """<Keywords>({result}[^<]+)<\/Keywords>""",
         """<Execution\sProcessID\\*='({process_id}[^']+)'""",
         """ThreadID\\*='({thread_id}[^']+)'""",
         """<Message>({additional_info}[^\n]+?)\s*<\/Message>"""
  ]
  DupFields = [ "event_name->operation"]


}
```