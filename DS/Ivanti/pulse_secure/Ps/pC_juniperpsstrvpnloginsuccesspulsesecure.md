#### Parser Content
```Java
{
Name = "juniper-ps-str-vpn-login-success-pulsesecure"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ Login succeeded for """
  """PulseSecure: """
]
Fields = [
  """PulseSecure:[\s\-]{0,100}({time}\d\d\d\d\-\d\d\-\d\d\s*\d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)\s*"""
  """({event_name}Login succeeded) for ({user}[^\/]+)\/({realm}[^\s]+) from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """PulseSecure:[^\[]+\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\(]+)|({user}[^\s\\]+))\(({realm}[^\)]+)?"""
]
DupFields = [
  "host->dest_host"
  "user->account"
]
ParserVersion = "v1.0.0"


}
```