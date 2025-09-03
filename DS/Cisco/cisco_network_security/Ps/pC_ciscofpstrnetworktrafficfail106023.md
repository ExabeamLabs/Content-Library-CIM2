#### Parser Content
```Java
{
Name = cisco-fp-str-network-traffic-fail-106023
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """%FTD-""", """-106023""", """Deny """, """ by access-group""" ]
  Fields = [
    """({time}[a-zA-Z]{3} \d\d (\d\d\d\d )?\d\d:\d\d:\d\d)""",
    """\s(({host}[\w.\-]+))\s*:\s*(\w+\s|%FTD\-)"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}({action}Deny)\s+({protocol}\w+))""",
    """\ssrc\s+({src_interface}[^:]+?):({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
    """\sdst\s+({dest_interface}[^:]+?):({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?""",
    """by access-group(\s+"+({access_group}[^\s"]+))?"""
  ]


}
```