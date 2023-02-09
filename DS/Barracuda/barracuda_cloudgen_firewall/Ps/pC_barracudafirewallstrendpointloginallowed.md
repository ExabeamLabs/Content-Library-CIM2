#### Parser Content
```Java
{
Name = barracuda-firewall-str-endpoint-login-allowed
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ LOGIN ATTEMPT: """, """ Info """, """ : Allowed""", """box_Auth_access:""", """: Login """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """Login (|({user}[^\s]+)\s)from ({src_ip}[a-fA-F\d:.]+)\s*:\s*({action}[^:.]+)(:|\.)""",
    """({event_name}LOGIN ATTEMPT)"""
  ]
  ParserVersion = "v1.0.0"


}
```