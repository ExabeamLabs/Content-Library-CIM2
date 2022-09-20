#### Parser Content
```Java
{
Name = citrix-netscalerwaf-str-network-traffic-ssl-handshake
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Netscaler WAF
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """ : default""", """ Backend """, """ ServerIP """, """-PPE""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({event_name}[^\s]+)""",
    """ServerIP\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """ServerPort\s*({src_port}\d+)""",
    """({result}SERVER AUTHENTICATED)"""
  ]
  DupFields = [ "event_name->operation" ]


}
```