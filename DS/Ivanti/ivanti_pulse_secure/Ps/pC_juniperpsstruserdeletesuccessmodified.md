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
  """PulseSecure:.+?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) - (::ffff:)?({host}\S+) - \[(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\] (({domain}[^\\]+)\\)?(System|({user}[\w\.\-]{1,40}\$?))"""
  """Removed username (({dest_domain}[^\\]+)\\)?({dest_user}[^\\\s]+)"""
]
DupFields = [
"dest_user->account_name"
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```