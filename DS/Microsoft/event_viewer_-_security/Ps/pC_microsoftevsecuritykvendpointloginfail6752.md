#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-675-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """EventCode=675"""
  """Pre-authentication failed:"""
]
Fields = [
  """({event_name}Pre-authentication failed)"""
  """ComputerName =({host}[\w.\-]+)"""
  """EventCode=({event_code}\d+)"""
  """User Name:\s+({user}.+?)\s+User ID:\s+({user_sid}.+?)\s+Service Name"""
  """Service Name:\s+\w+\/(?=\w)({domain}.+?)\s+Pre-Authentication"""
  """Failure Code:\s+({result_code}[\w]+)"""
  """Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```