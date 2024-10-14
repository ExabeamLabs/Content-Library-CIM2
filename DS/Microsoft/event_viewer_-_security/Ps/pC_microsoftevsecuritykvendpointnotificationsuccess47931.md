#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4793-1
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat =  "epoch"
  Conditions = [ """EventIDCode=4793""", """The Password Policy Checking API was called""" ]
  Fields = [
    """TimeGenerated=({time}\d{13})""",
    """({event_name}The Password Policy Checking API was called)""",
    """EventIDCode=({event_code}\d+)""",
    """Computer=({host}[\w\-.]+)""",
    """User=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """Domain=(|({domain}[^\s]+))\s""",
    """EventType=(|({event_category}[^\s]+))\s""",
    """EventCategory=({operation_type}\S+)""",
    """RecordNumber=({event_id}\S+)""",
    """Security ID:\s*(SYSTEM|({user_sid}\S+))""",
    """Account Name:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT Service|({domain}[^\s]+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Additional Information:""",
    """Status Code:\s*({action}\S+)""",
  ]


}
```