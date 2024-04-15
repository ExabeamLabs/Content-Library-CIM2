#### Parser Content
```Java
{
Name = "cyberark-pam-mix-user-switch-success-retrievepassword"
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """|Cyber-Ark|Vault|"""
  """Action=Retrieve password"""
  """Safe"""
]
Fields = [
  """(\d\d:\d\d:\d\d|\d\d\d\d-\d\d-\d\d\w\d\d:\d\d:\d\d\w) ({host}[\w\-.]+) (LEEF|CEF)""",
  """(LEEF|CEF):([^\|]*?\|){4}({event_code}\d+)""",
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
  """usrName =(({domain}[^\\=]+)(\\)+)?(({email_address}[^@"\.]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^=]+?))\s+\w+=""",
  """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """\sFile=[^=]+\-({dest_user}[^\s-]+)\s+\w+=""",
  """\sFile=(({domain}[^\\]+)\\)?({dest_user}[^=]+?)\s+\w+=""",
  """\sSafe=({safe_value}[^=]+?)\s+\w+=""",
  """\sGatewayStation=({gateway_station}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  """\sReason=({reason}[^=]+?)\s+\w+=""",
  """\sAction=({action}[^=]+?)\s+\w+=""",
]
DupFields = [
  "host->dest_host",
  "dest_user->account"
]
ParserVersion = "v1.0.0"


}
```