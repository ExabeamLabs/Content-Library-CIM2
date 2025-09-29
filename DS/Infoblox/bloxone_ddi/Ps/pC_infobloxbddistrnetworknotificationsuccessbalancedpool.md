#### Parser Content
```Java
{
Name = infoblox-bddi-str-network-notification-success-balancedpool
  ParserVersion = v1.0.0
  Conditions = [ """dhcpd[""", """: balanced pool""" ]

s-infoblox-one-dhcp-dl-events = {
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+dhcpd\[""",
    """dhcpd\[\S+?:\s+({additional_info}[^~]+?)\s*$"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  
}
```