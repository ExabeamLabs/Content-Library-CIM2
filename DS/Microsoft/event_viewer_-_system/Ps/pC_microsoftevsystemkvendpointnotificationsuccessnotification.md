#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-endpoint-notification-success-notification
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat =  "epoch_sec"
  Conditions = [ """EventIDCode=""", """Computer=""", """RecordNumber=""", """TimeGenerated=""", """Message=""" ]
  Fields = [
    """TimeGenerated="?({time}\d{10})"?""",
    """Message=\s*"?({event_name}.+?)"?\.\s+\[?""",
    """EventIDCode="?({event_code}\d+)"?""",
    """Computer="?({host}[\w\-.]+)"?""",
    """User="?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"?\s""",
    """Domain="?(|({domain}[^\s"]+?))\s*"?\s""",
    """EventType="?(|({event_category}[^\s"]+?))\s*"?\s""",
    """EventCategory="?({operation_type}\S+?)"?\s""",
    """RecordNumber="?({event_id}\S+?)"?\s""",
    """Requester:\s*(({account_domain}[^\s\\]+)\\+)?({account_name}[\w\-\.]+\$?)\s""",
    """Attributes:\s*({attributes}[^"$]+)\s*$"""
    """Client Port:\s*(\\r|\\n|\\t)*({src_port}\d+)"""
    """Failure Code(:|=)\s*(\\r|\\n|\\t)*({result_code}[\w]+)"""
    """Client Address(:|=)\s*(\\r|\\n|\\t)*(::[\w]+:)?(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """Service Name(:|=)\s*(\\[rnt])*(\w+\/(?=\w))?({domain}[^\s]+?)\s*;*(\\+[rnt]|\s)*Network Information"""
    """Service Name(:|=)\s*(\w+\/(?=\w))?(\\t)+?(({account}[^\\\/"]+)[\\\/]+)?({domain}[^\\\/].+?)\s*;*(\\[rnt]|\s)*Network Information:"""
    """Account Name(:|=)\s*(\\r|\\n|\\t)*?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\r\s\\r\s\\n)?Service Information:"""
    """Account Information(:|=)\s*;*(\\r|\\n|\\t)*Security ID(:|=)\s*(\\r|\\n|\\t)*({user_sid}.+?)\s*;*(\\r|\\n|\\t)*Account"""
  ]
    DupFields = [
    "result_code->failure_code"
    "user->account"
  ]


}
```