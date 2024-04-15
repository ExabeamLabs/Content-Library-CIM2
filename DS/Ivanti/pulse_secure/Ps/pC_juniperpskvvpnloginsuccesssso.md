#### Parser Content
```Java
{
Name = "juniper-ps-kv-vpn-login-success-sso"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ PulseSecure:"""
  """Web SSO:"""
  """ Authentication successful"""
]
Fields = [
    """(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+))\s+(Juniper|PulseSecure):""",
    """PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
    """PulseSecure:.*?\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\s]+)|({user}[^\s]+))\(({realm}[^\)]+)?"""
  ]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```