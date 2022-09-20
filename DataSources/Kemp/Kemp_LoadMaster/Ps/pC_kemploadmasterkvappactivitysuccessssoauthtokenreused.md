#### Parser Content
```Java
{
Name = kemp-loadmaster-kv-app-activity-success-ssoauthtokenreused
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "epoch"
Conditions = [
  """ssomgr: SSO-auth-token reused"""
]
Fields = [
  """\s({host}[\w\-\.]+)\s+\S+\s+\-\s+ssomgr:"""
  """\[host=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\[user=(({domain}[^\\]+)\\)?({user}[^\]]+)\]"""
  """\[user=({email_address}[^@]+@({email_domain}[^@\]\s]+))\]"""
  """\[user=({user}[^@]+@[^@\]\s]+)\]"""
  """\sssomgr:\s*({operation}.+?)\s*\["""
]
ParserVersion = "v1.0.0"


}
```