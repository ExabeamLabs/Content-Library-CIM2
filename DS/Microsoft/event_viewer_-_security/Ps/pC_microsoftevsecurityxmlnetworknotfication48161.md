#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-notfication-4816-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Conditions = [ """<EventID>4816<""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}RPC detected an integrity violation while decrypting an incoming message.)""",
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({dest_host}({host}[\w\-.]+))""",
    """<Execution ProcessID\\*="({process_id}\d+)" ThreadID\\*="({thread_id}\d+)"""",
    """<Data Name ="PeerName">({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<"""
    """<System>.*?Guid(\\)?="\{({process_guid}[^}]+)""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```