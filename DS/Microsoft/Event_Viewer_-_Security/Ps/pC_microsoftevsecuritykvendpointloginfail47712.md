#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-4771-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """LogType="WLS"""", """EventID="4771"""" ]
  Fields = [
    """Computer="+({dest_host}[^"]+)"""",
    """EventID="+({event_code}[^"]+)"""",
    """EventRecordID="+({event_id}[^"]+)"""",
    """IpAddress="+(?:::[\w]+:)?({dest_ip}[a-fA-F:\d.]+)"""",
    """ServiceName ="+\w+\/(?=\w)({domain}[^"]+)"""",
    """Status="+({result_code}[^"]+)"""",
    """TargetSid="+({user_sid}[^"]+)"""",
    """TargetUserName ="+(?=\w)({user}[^"]+)""""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```