#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-endpoint-notification-success-255"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSS"]
Conditions = ["""<EventID>255</EventID>""","""'Microsoft-Windows-Sysmon'"""]
Fields = [
  """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """<Data Name\\*='UtcTime'>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)<\/Data>"""
  """<Computer>({host}[^<]+)<\/Computer>""",
  """<EventID>({event_code}\d+)<\/EventID>""",
  """<Security UserID\\*='({user_sid}[^']+)'"""
  """({log_name}Microsoft-Windows-Sysmon)"""
  """<Data Name\\*='Description('|")>({additional_info}[^<]+?)\s*(\\n)?</Data>"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```