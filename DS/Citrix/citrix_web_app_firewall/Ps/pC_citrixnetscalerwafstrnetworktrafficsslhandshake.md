#### Parser Content
```Java
{
Name = citrix-netscalerwaf-str-network-traffic-ssl-handshake
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Web App Firewall
  TimeFormat = "MM/dd/yyyy:HH:mm:ss z"
  Conditions = [ """ : default""", """ Backend """, """ ServerIP """, """-PPE""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d\s*GMT)\s({host}[^\s]+).*?:\sdefault\s({protocol}[^\s]+)\s({operation}({event_name}[^\s]+))""",
    """ServerIP\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ServerPort\s*({src_port}\d+)""",
    """({result}SERVER AUTHENTICATED)"""
  ]


}
```