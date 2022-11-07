#### Parser Content
```Java
{
Name = barracuda-firewall-str-endpoint-login-fail-denied
  Vendor = Barracuda
  Product = Barracuda Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ LOGIN ATTEMPT: """, """ Security """, """: Denied: """, """: Login """, """box_Auth_access:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """Login (|({user}[^\s]+)\s)from ({src_ip}[a-fA-F\d:.]+)\s*:\s*({action}[^:.]+)(:|\.)""",
    """({event_name}LOGIN ATTEMPT)"""
  """Denied:\s({failure_reason}[^$]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```