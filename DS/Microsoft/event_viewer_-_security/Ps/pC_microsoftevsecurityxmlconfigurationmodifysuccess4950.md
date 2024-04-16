#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-configuration-modify-success-4950"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [ """<EventID>4950<""", """Microsoft-Windows-Security-Auditing""", """<Computer>"""]
Fields = [
  """<TimeCreated SystemTime=('|")({time}\d{4}\-\d{2}\-\d{2}T\d+:\d+:\d+.\d+Z)""",
  """({event_code}4950)""",
  """<Computer>({host}[\w\-.]+)</Computer>"""
  """<Keywords>({result}[^<]+)</Keywords>""",
  """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)""",
  """<Data Name =('|")SettingType('|")>({additional_info}[^<]+)</Data>"""
]
DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```