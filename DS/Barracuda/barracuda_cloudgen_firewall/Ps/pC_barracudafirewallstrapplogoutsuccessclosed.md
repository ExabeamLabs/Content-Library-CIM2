#### Parser Content
```Java
{
Name = barracuda-firewall-str-app-logout-success-closed
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  ParserVersion = v1.0.0
  TimeFormat = """yyyy-MM-dd HH:mm:ss"""
  Conditions = [ """: Closed """, """ Info """, """box_Auth_access:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """box_control\[\d+\]:\s*({additional_info}[^$]+?)\s*$""",
    """Session ({src_host}[^:]+): Closed"""
  ]


}
```