#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-http-request-success-1102
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat =  "epoch"
  Conditions = [ """EventIDCode=1102""", """The Federation Service authorized a request to one of the REST endpoints""" ]
  Fields = [
    """TimeGenerated=({time}\d+)""",
    """({event_name}The Federation Service authorized a request to one of the REST endpoints)""",
    """EventIDCode=({event_code}\d+)""",
    """Computer=({host}[\w\-.]+)""",
    """User=(|({user}[^\s]+))\s""",
    """Domain=(|({domain}[^\s]+))\s""",
    """EventType=(|({event_category}[^\s]+))\s""",
    """EventCategory=({operation_type}\S+)""",
    """RecordNumber=({event_id}\S+)""",
    """Client IP:\s*({src_ip}[A-Fa-f:\d.]+)""",
    """Security ID:\s*(SYSTEM|({user_sid}[^\s]+))\s""",
  ]


}
```