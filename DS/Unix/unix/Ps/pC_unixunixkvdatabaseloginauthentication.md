#### Parser Content
```Java
{
Name = "unix-unix-kv-database-login-authentication"
Vendor = "Unix"
Product = "Unix"
TimeFormat = ["MMM dd HH:mm:ss","MMM d HH:mm:ss"]
Conditions = [
  """ authentication: """
  """(postgresql:auth)"""
  """journal"""
]
Fields = [
  """:\s+({time}\w+\s+\d+ \d\d:\d\d:\d\d)""",
  """ruser=((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s"""
  """({host}[\w\.\-]+)?:?\s*journal\s*\[({process_id}[^\]]+)\]"""
  """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\((({src_port}\d+[^\)])+)\)\s*authentication:"""
  """\(postgresql:auth\):\s({event_name}[^;]+);"""
  """\suid=({user_id}[^\s]+)\s"""
  """\srhost=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))\s"""
  """\suser=((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*("|$)"""
  """:\s+authentication\s+({result}[^;]+);"""
  """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+"""
  ]
ParserVersion = "v1.0.0"


}
```