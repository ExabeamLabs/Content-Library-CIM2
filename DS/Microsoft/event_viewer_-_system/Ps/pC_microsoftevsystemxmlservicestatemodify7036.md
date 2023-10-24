#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-service-state-modify-7036"
  Vendor = "Microsoft"
  Product = "Event Viewer - System"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """>7036</EventID>"""
  """<Data Name""",
  """ service entered the running state."""
  ]
  Fields = [
    """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """ProcessID\\*=('|")({process_id}[^'"]+)"""
    """<Computer>({src_host}({host}[^<]+))</Computer>"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
    """>({event_code}\d+)</EventID>"""
    """<Message>({event_name}The.+?)<"""
    """<Data Name =('|")param1('|")>({service_name}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```