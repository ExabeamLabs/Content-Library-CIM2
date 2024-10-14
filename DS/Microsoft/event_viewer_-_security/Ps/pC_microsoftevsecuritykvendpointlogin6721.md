#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-672-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """EventCode=672"""
  """Service Name:"""
  """krbtgt"""
]
Fields = [
  """({event_name}Account Logon)"""
  """ComputerName =({host}[\w.\-]+)"""
  """EventCode=({event_code}\w+)"""
  """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Supplied Realm Name:\s+({domain}[^\s]+)"""
  """Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Result Code:\s+({result_code}[\w\-]+)"""
  """Sid=({user_sid}[^\s]+)\s+SidType"""
]
ParserVersion = "v1.0.0"


}
```