#### Parser Content
```Java
{
Name = "cyberark-pam-mix-user-switch-success-retrievepassword"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
Conditions = [
  """|Cyber-Ark|Vault|"""
  """Action=Retrieve password"""
  """Safe"""
]
Fields = [
  """(\d\d:\d\d:\d\d|\d\d\d\d-\d\d-\d\d\w\d\d:\d\d:\d\d\w) ({host}[\w\-.]+) (LEEF|CEF)""",
  """(LEEF|CEF):([^\|]*?\|){4}({event_code}\d+)""",
  """({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d))\s*({host}[\w\-.]+)\s*LEEF"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
  """usrName =(({domain}[^\\=]+)(\\)+)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=""",
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """\sFile=[^=]+\-({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
  """\sFile=(({domain}[^\\]+)\\)?[^\-]+\-({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
  """\sSafe=({safe_value}[^=]+?)\s+\w+=""",
  """\sGatewayStation=({gateway_station}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  """\sReason=({result_reason}[^=]+?)\s+\w+=""",
  """\sAction=({action}[^=]+?)\s+\w+=""",
]
DupFields = [
  "host->dest_host",
  "dest_user->account"
]
ParserVersion = "v1.0.0"


}
```