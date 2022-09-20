#### Parser Content
```Java
{
Name = cisco-ise-kv-vpn-login-success-radiusaccounting
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CSCOacs_RADIUS_Accounting""", """RADIUS Accounting start request,""", """Acct-Status-Type=Start""", """NAS-Port-Type=Virtual""" ]
  Fields = [
    """\d+\s+({time}\d\d\d\d\-\d\d\-\d\d \d+:\d+:\d+)""",
    """CSCOacs_RADIUS_Accounting\s+(\d+\s+){3}\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """({dest_host}[^\s]+)\s+CSCOacs_RADIUS_Accounting""",
    """,\s*User-Name =(({domain}[^\s\\\/]+)[\\\/]+)?(?:(\w{2}\-){5}\w{2}|({user}[^,]+))""",
    """Tunnel-Client-Endpoint=\(.+?\)\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """Framed-IP-Address=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),"""
    """,\s*Device IP Address=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\:\d\d\s({dest_host}.+?)\sCSCOacs"""
  ]
  ParserVersion = "v1.0.0"


}
```