#### Parser Content
```Java
{
Name = microsoft-evsystem-json-process-close-5186
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [  """"EventID":5186""", """Microsoft-Windows-WAS""" ]
  Fields = [
     """(Hostname|Computer)":\s*"({host}[^"]+)""",
     """EventTime":\s*"({time}[^"]+)""",
     """({event_code}5186)""",
     """ExecutionProcessID":\s*({process_id}\d+)""",
     """Message":\s*"({additional_info}[^"]+)"""",
     """RecordNumber":\s*({event_id}\d+)""",
     """ProcessID":\s*"({process_id}[^"]+)""",
     """EventType":\s*"({event_category}[^"]+)""",
     """Severity":\s*"({severity}[^"]+)""""
  ]
  DupFields = ["additional_info->event_name"]


}
```