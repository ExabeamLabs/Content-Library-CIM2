#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-policy-apply-4954
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat =  "epoch"
  Conditions = [ """EventIDCode=4954""", """Group Policy settings for Windows Firewall were changed, and the new settings were applied""" ]
  Fields = [
    """TimeGenerated=({time}\d+)""",
    """({event_name}Group Policy settings for Windows Firewall were changed, and the new settings were applied)""",
    """EventIDCode=({event_code}\d+)""",
    """Computer=({host}[\w\-.]+)""",
    """User=(|({user}[^\s]+))\s""",
    """Domain=(|({domain}[^\s]+))\s""",
    """EventType=(|({event_category}[^\s]+))\s""",
    """EventCategory=({operation_type}\S+)""",
    """RecordNumber=({event_id}\S+)""",
  ]


}
```