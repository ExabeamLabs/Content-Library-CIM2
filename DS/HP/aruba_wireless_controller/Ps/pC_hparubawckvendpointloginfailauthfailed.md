#### Parser Content
```Java
{
Name = "hp-arubawc-kv-endpoint-login-fail-authfailed"
Vendor = "HP"
Product = "Aruba Wireless controller"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """authmethod="""
  """servername="""
  """apname="""
  """bssid="""
  "Authentication failed"
]
Fields = [
  """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\+"""
  """\d\d:\d\d:\d\d\s+(\d\d\d\d\s+)?({host}[^\s]+)\s(authmgr|stm|dot1x-proc:\d+)\[({event_code}\d+)\]""",
  """username=(host\/({src_host}[\w\-.]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\)?({=user}[^\s]+))\s+\w+="""
  """userip=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """usermac=({src_mac}[a-f0-9:]+)"""
  """bssid=(({dest_mac}([0-9a-fA-F]{1,2}[.:-]){5}([0-9a-fA-F]{1,2}))|({dest_host}[\w\-.]+))"""
  """servername=(Internal|({dest_host}[\w\-.]+))\s""",
  """serverip=({auth_server}[a-f0-9.]+)"""
  """authmethod=({auth_method}[^\s]+)"""
  """User\sAuthentication\s({result}[\w]+)"""
]
ParserVersion = "v1.0.0"


}
```