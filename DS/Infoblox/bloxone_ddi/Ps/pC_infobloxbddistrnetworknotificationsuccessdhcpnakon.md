#### Parser Content
```Java
{
Name = infoblox-bddi-str-network-notification-success-dhcpnakon
  ParserVersion = v1.0.0
  Conditions = [ """dhcpd[""", """: DHCPNAK on""", """via""" ]
  Fields = ${DLUnixParsersTemplates.s-infoblox-one-dhcp-dl-events.Fields}[
  """DHCPNAK on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? to ({dest_mac}[A-Fa-f:\d.]+) via ({dest_interface}[^\s"]+)""",
  """({event_name}DHCPNAK)"""
  ]

s-infoblox-one-dhcp-dl-events = {
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+dhcpd\[""",
    """dhcpd\[\S+?:\s+({additional_info}[^~]+?)\s*$"""
  
}
```