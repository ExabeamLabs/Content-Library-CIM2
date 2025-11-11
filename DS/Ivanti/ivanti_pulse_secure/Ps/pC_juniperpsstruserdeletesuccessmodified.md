#### Parser Content
```Java
{
Name = "juniper-ps-str-user-delete-success-modified"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""PulseSecure:"""
"""User Accounts modified."""
]
Fields = [
  """PulseSecure:.+?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) - (::ffff:)?({dest_host}({host}\S+)) - \[(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\] (({domain}[^\\\(]+)\\)?(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """Removed username (({dest_domain}[^\\]+)\\)?({account_name}({dest_user}[^\\\s]+))"""
]
ParserVersion = "v1.0.0"


}
```