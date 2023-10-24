#### Parser Content
```Java
{
Name = "pan-gp-leef-vpn-login-success-gatewayuser"
  ParserVersion = "v1.0.0"
  Conditions = ["""subtype=globalprotect""","""globalprotectgateway""","""Palo Alto Networks""", """GlobalProtect gateway user login succeeded""" ]

q-pan-vpn-parser = {
  Vendor = "Palo Alto Networks"
  Product = "GlobalProtect"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """User name:\s+({user}[\w\.\-]{1,40}\$?)\.?(\s|,|"|$)""",
    """User name:\s+({email_address}[^@\s]+@[^\s,]+),""",
    """\|devTime=({time}\w{3}\s+\d+ \d\d\d\d \d\d:\d\d:\d\d \w+)\|""",
    """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """DeviceName =({host}[\w\-.]+)""",
    """Client OS( version)?:\s+({os}[^":]+)(,|\.)""",
    """Login from:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  
}
```