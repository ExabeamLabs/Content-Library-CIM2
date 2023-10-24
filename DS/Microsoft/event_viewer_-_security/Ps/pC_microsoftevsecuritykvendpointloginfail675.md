#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-675"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """LogType=\"WLS\""""
  """EventID=\"675\""""
]
Fields = [
  """({event_name}Pre-authentication failed)"""
  """Computer=\"+({dest_host}[\w\-.]+)\""""
  """EventID=\"+({event_code}[^\"]+)\""""
  """EventRecordID=\"+({event_id}[^\"]+)\""""
  """IpAddress=\"+(?:::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
  """ServiceName =\"+\w+\/(?=\w)({domain}[^\"]+)\""""
  """Status=\"+({result_code}[^\"]+)\""""
  """TargetSid=\"+({user_sid}[^\"]+)\""""
  """TargetUserName =\"+(?=\w)({user}[\w\.\-]{1,40}\$?)\""""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```