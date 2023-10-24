#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-675-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """(675)"""
  """Pre-authentication failed"""
]
Fields = [
  """({time}\w+ \d{1,2} [\d:]+ \d+):"""
  """({event_name}Pre-authentication failed)"""
  """({host}[\w\-.]+)\/Security \(({event_code}675)\)"""
  """User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+User ID:\s\%\{({user_sid}[^}]+)\}"""
  """Service Name:\s+\w+\/(?=\w)({domain}.+?)\s+Pre-Authentication"""
  """Failure Code:\s+({result_code}[\w]+)"""
  """Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "host->dest_host"
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```