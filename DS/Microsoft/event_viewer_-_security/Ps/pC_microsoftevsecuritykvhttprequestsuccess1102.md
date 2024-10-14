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
    """TimeGenerated=({time}\d{13})""",
    """({event_name}The Federation Service authorized a request to one of the REST endpoints)""",
    """EventIDCode=({event_code}\d+)""",
    """Computer=({dest_host}({host}[\w\-.]+))""",
    """User=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """Domain=(|({domain}[^\s]+))\s""",
    """EventType=(|({event_category}[^\s]+))\s""",
    """EventCategory=({operation_type}\S+)""",
    """RecordNumber=({event_id}\S+)""",
    """Client IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Security ID:\s*(SYSTEM|({user_sid}[^\s]+))\s""",
  ]


}
```