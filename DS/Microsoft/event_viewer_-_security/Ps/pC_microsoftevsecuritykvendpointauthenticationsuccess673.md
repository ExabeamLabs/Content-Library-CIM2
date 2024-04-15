#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-authentication-success-673"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "E MMM dd HH:mm:ss yyyy"
Conditions = [
  """User Name:"""
  """(673)"""
]
Fields = [
  """EvntSLog:\s+\[.+\]\s+({time}\w+ \w+ \d+ \d+:\d+:\d+ \d+):\s+({host}[\w. /\\]+)\/.*\s+\(({event_code}\w+)\)"""
  """User Name:\s+({user}[^@]+)@({domain}[^\s]+)"""
  """Service Name:\s+({dest_host}\S+\$)\s"""
  """Service Name:\s+({service_name}\S+)"""
  """Client Address:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Failure Code:\s+({result_code}[\w\-]+)"""
  """Ticket Options:\s+({ticket_options}[^\s]+)"""
  """Ticket Encryption Type:\s+({ticket_encryption_type}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```