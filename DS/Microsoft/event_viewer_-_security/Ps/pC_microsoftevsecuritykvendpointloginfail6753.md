#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-675-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EventIDCode=675"""
]
Fields = [
  """({event_name}Pre-authentication failed)"""
  """TimeGenerated=({time}\d{10})"""
  """Computer=({host}[^\s]+)"""
  """EventID=({event_code}\d+)"""
  """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+User ID:\s+({user_sid}.+?)\s+Service Name"""
  """Service Name:\s+\w+\/(?=\w)({domain}.+?)\s+Pre-Authentication"""
  """Failure Code:\s+({result_code}[\w]+)"""
  """Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```