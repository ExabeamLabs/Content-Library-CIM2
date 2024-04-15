#### Parser Content
```Java
{
Name = "cyberark-pam-mix-user-password-modify-success-changepassword"
ParserVersion = v1.0.0
Vendor = "CyberArk"
Product = "Cyberark Privilege Access Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """|Cyber-Ark|Vault|"""
  """Action=CPM Change Password"""
  """Safe"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({host}[\w\-.]+) (LEEF|CEF)""",
  """(LEEF|CEF):([^\|]*?\|){4}({event_code}\d+)""",
  """usrName =(({domain}[^\\\/=]+)(\\\/)+)?(({email_address}[^@=]+@[^.=]+\.[^=]+?)|({user}[^=]+?))\s+\w+=""",
  """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """\sFile=({account}.+?)\s+\w+=""",
  """\sFile=[^=]+\-({account}\w{1,11})\s+\w+=""",
  """\sSafe=({safe_value}.+?)\s+\w+=""",
  """\sGatewayStation=({gateway_station}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  """\sReason=({reason}[^=]+?)\s+\w+=""",
  """\sExtraDetails=address=((\d{1,3}\.){3}\d{1,3}|({src_host}[^;]+));username=({account}[^;]+)""",
  """Action=({action}[^=]+?)\s+\w+="""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```