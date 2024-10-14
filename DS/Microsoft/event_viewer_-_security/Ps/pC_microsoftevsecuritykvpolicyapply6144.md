#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-policy-apply-6144
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat =  "epoch"
  Conditions = [ """EventIDCode=6144""", """Security policy in the group policy objects has been applied successfully""" ]
  Fields = [
    """TimeGenerated=({time}\d{13})""",
    """({event_name}Security policy in the group policy objects has been applied successfully)""",
    """EventIDCode=({event_code}\d+)""",
    """Computer=({host}[\w\-.]+)""",
    """User=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """Domain=(|({domain}[^\s]+))\s""",
    """EventType=(|({event_category}[^\s]+))\s""",
    """EventCategory=({operation_type}\S+)""",
    """RecordNumber=({event_id}\S+)""",
    """Return Code:\s*({return_code}\S+)""",
  ]


}
```