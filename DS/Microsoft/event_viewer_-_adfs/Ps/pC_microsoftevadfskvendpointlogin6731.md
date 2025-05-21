#### Parser Content
```Java
{
Name = "microsoft-evadfs-kv-endpoint-login-673-1"
Vendor = "Microsoft"
Product = "Event Viewer - ADFS"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """EventCode=673"""
  """User Name:"""
]
Fields = [
  """({event_name}Account Logon)"""
  """ComputerName =({host}[\w.\-]+)"""
  """EventCode=({event_code}\w+)"""
  """User Name:\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[\w._\-]+))?\s+Supplied Realm"""
  """Service Name:\s+({dest_host}\S+\$)\s"""
  """Service Name:\s+({service_name}\S+)"""
  """Client Address:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Failure Code:\s+({result_code}[\w\-]+)"""
  """Sid=({user_sid}[^\s]+)\s+SidType"""
  """Ticket Options:\s+({ticket_options}[^\s]+)"""
  """Ticket Encryption Type:\s+({ticket_encryption_type}[^\s]+)"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```