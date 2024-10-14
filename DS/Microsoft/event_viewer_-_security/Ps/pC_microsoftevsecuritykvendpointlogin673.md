#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-673"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EventIDCode=673"""
]
Fields = [
  """EventID=({event_code}\d+).+?User Domain:\s+({domain}[^\s]+)"""
  """TimeGenerated=({time}\d{10})"""
  """Computer=({host}[^\s]+)"""
  """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?).+?Service Name:\s+({service_name}\S+).+?Client Address:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+?Failure Code:\s+({result_code}[^\s]+)"""
  """Service Name:\s+({dest_host}\S+\$)\s"""
  """Ticket Options:\s+({ticket_options}[^\s]+)"""
  """Ticket Encryption Type:\s+({ticket_encryption_type}[^\s]+)"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```