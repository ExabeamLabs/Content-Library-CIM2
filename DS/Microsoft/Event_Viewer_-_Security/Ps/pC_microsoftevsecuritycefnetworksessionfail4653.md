#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-network-session-fail-4653
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """"eventID":"4653"""", """An IPsec main mode negotiation failed""" ]
  Fields = [
    """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"computer":"({host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+?)\s*"""",
    """"eventID":"({event_code}\d+)""",
    """"eventRecordID":"({event_id}\d+)""",
    """"severityValue":"({action}[^"]+?)\s*"""",
    """"failureReason":"({failure_reason}[^"]+?)[\s\\r\\n]*"""",
    """"localAddress":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"remoteAddress":"({src_ip}[A-Fa-f:\d.]+)""",
    """"localKeyModPort":"({dest_port}\d+)""",
    """"remoteKeyModPort":"({src_port}\d+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```