#### Parser Content
```Java
{
Name = cisco-ise-kv-radius-traffic-success-start
Vendor = Cisco
Product = Cisco ISE
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CSCOacs_RADIUS_Accounting"""
  """RADIUS Accounting start request,"""
  """Acct-Status-Type=Start"""
]
Fields = [
  """\d+\s+({time}\d\d\d\d\-\d\d\-\d\d \d+:\d+:\d+)"""
  """CSCOacs_RADIUS_Accounting\s+(\d+\s+){3}\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """({host}[^\s]+)\s+CSCOacs_RADIUS_Accounting"""
  """,\s*User-Name =(({domain}[^\s\\\/]+)(\/+|\\+))?(?:(\w{2}\-){5}\w{2}|({user}[^,]+))"""
  """,\s*Calling-Station-ID=({dest_host}[^,]+)"""
  """,\s*AD-Host-Resolved-Identities=({dest_host}[^@,]+)"""
  """,\s*Device IP Address=({auth_server}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """,\s*Device IP Address=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """,\s*Framed-IP-Address=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```