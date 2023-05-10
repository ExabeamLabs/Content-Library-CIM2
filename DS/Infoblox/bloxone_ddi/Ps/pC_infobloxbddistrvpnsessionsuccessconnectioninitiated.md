#### Parser Content
```Java
{
Name = infoblox-bddi-str-vpn-session-success-connectioninitiated
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """openvpn-master[""", """Peer Connection Initiated with [AF_INET]""" ]
  Fields = [
     """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}[a-fA-F\d.:]+?)\s+({additional_info}[^~]+?)\s*$""",
     """({event_name}Peer Connection Initiated) with [^\]]+\]({dest_ip}[a-fA-F\d.:]+?):({dest_port}\d+)"""

  ]
  ParserVersion = "v1.0.0"


}
```