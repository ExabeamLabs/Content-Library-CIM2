#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-policy-modify-4946-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4946</EventID>""", """<Provider Name""","""'Microsoft-Windows-Security-Auditing'"""  , """<Event xmlns"""]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Correlation ActivityID\\*='\{({activity_id}[^\}']+)""",
    """<Execution ProcessID\\*='({process_id}[^']+)""",
    """<Data Name\\*='RuleId'>\{?({rule_id}[^}<]+)""",
    """<Data Name\\*='RuleName'>({rule}[^<]+)""",
    """ThreadID\\*='({thread_id}[^']+)""",
    """<Keywords?>({result}[^<]+)<\/Keywords?>"""  
  ]


}
```