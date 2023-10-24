#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-endpoint-notification-success-notification
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat =  "epoch"
  Conditions = [ """EventIDCode=""", """Computer=""", """RecordNumber=""", """TimeGenerated=""", """Message=""" ]
  Fields = [
    """TimeGenerated="?({time}\d{13})"?""",
    """Message=\s*"?({event_name}.+?)"?\.\s+\[?""",
    """EventIDCode="?({event_code}\d+)"?""",
    """Computer="?({host}[\w\-.]+)"?""",
    """User="?(|({user}[\w\.\-]{1,40}\$?))\s*"?\s""",
    """Domain="?(|({domain}[^\s"]+?))\s*"?\s""",
    """EventType="?(|({event_category}[^\s"]+?))\s*"?\s""",
    """EventCategory="?({operation_type}\S+?)"?\s""",
    """RecordNumber="?({event_id}\S+?)"?\s""",
  ]


}
```