#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-authentication-success-authenticationsuccess"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """: authentication success"""
  """pam_sss(sudo"""
]
Fields = [
  """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """ruser=((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  """\s({host}[\w\.\-]+)?:?\s*sudo"""
  """:\s({event_name}[^;]+);"""
  """\suid=({user_id}[^\s]+)\s"""
  """\srhost=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))\s"""
  """\suser=((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s|\"|$)"""
  """:\s+authentication\s+({result}success);"""
  ]
ParserVersion = "v1.0.0"


}
```