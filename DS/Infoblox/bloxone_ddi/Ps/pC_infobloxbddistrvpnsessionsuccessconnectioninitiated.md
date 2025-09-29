#### Parser Content
```Java
{
Name = infoblox-bddi-str-vpn-session-success-connectioninitiated
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """openvpn-master[""", """Peer Connection Initiated with [AF_INET]""" ]
  Fields = [
     """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?\s+({additional_info}[^~]+?)\s*$""",
     """({event_name}Peer Connection Initiated) with [^\]]+\]({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?):({dest_port}\d+)"""
     """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+"""
     """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""

  ]
  ParserVersion = "v1.0.0"


}
```