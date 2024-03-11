#### Parser Content
```Java
{
Name = kemp-loadmaster-kv-app-activity-success-ssoauthtokenreused
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ssomgr: SSO-auth-token reused"""
]
Fields = [
  """\s({host}[\w\-\.]+)\s+\S+\s+\-\s+ssomgr:"""
  """\[host=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\[user=(({domain}[^\\]+)\\)?({user}[^\]]+)\]"""
  """\[user=({email_address}[^@]+@({email_domain}[^@\]\s]+))\]"""
  """\[user=({user}[^@]+@[^@\]\s]+)\]"""
  """\sssomgr:\s*({operation}.+?)\s*\["""
]
ParserVersion = "v1.0.0"


}
```