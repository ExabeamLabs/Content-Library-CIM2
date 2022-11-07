#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-policy-apply-fail-6145
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat =  "epoch"
  Conditions = [ """EventIDCode=6145""", """One or more errors occured while processing security policy in the group policy objects""" ]
  Fields = [
    """TimeGenerated=({time}\d+)""",
    """({event_name}One or more errors occured while processing security policy in the group policy objects)""",
    """EventIDCode=({event_code}\d+)""",
    """Computer=({host}[\w\-.]+)""",
    """User=(|({user}[^\s]+))\s""",
    """Domain=(|({domain}[^\s]+))\s""",
    """EventType=(|({event_category}[^\s]+))\s""",
    """EventCategory=({operation_type}\S+)""",
    """RecordNumber=({event_id}\S+)""",
    """Error Code:\s*({error_code}\S+)""",
  ]


}
```