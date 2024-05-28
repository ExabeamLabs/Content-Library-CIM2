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
    """Computer="+({host}[\w\-.]+)"""",
    """EventID="+({event_code}[^"]+)"""",
    """EventRecordID="+({event_id}[^"]+)"""",
    """IpAddress="+(?:::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """ServiceName ="+\w+\/(?=\w)({domain}[^"]+)"""",
    """Status="+({result_code}[^"]+)"""",
    """TargetSid="+({user_sid}[^"]+)"""",
    """TargetUserName ="+(?=\w)({user}[\w\.\-]{1,40}\$?)""""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```