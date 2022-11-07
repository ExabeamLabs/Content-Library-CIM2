#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-notfication-4816
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4816<""", """RPC detected an integrity violation while decrypting an incoming message""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}RPC detected an integrity violation while decrypting an incoming message.)""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID='({process_id}\d+)' ThreadID='({thread_id}\d+)'""",
    """Peer Name:\s+({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
  ]


}
```