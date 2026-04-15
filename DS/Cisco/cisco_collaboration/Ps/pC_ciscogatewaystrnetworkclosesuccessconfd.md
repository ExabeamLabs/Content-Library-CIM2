#### Parser Content
```Java
{
Name = "cisco-gateway-str-network-close-success-confd"
  Vendor = "Cisco"
  Product = "Cisco Collaboration"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssz"
  Conditions = [ """ confd """, """ audit user: """, """ terminated session""" ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)""",
    """:\d\d:\d\d[+-]\d\d:\d\d\s({host}[\w.-]+)""",
    """\s({process_name}confd)\s+({process_id}[^\s]+)""",
    """audit user:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\/({user_id}[^\s]+)""",
    """({event_name}({operation}terminated session))""",
    """reason:\s*({result_reason}[^"\)]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```