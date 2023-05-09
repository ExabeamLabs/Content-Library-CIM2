#### Parser Content
```Java
{
Name = barracuda-firewall-str-endpoint-login-fail-denied
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ LOGIN ATTEMPT: """, """ Security """, """: Denied: """, """: Login """, """box_Auth_access:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """Login (|({user}[^\s]+)\s)from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*:\s*({action}[^:.]+)(:|\.)""",
    """({event_name}LOGIN ATTEMPT)""",
    """Denied:\s({failure_reason}[^$]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```