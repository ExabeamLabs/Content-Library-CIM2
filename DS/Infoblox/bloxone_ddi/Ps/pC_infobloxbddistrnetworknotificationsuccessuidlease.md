#### Parser Content
```Java
{
Name = infoblox-bddi-str-network-notification-success-uidlease
  ParserVersion = v1.0.0
  Conditions = [ """dhcpd[""", """: uid lease""" ]
  Fields = ${DLUnixParsersTemplates.s-infoblox-one-dhcp-dl-events.Fields}[
  """for client ({dest_mac}[A-Fa-f:\d.]+)\s*is"""
  ]

s-infoblox-one-dhcp-dl-events = {
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+dhcpd\[""",
    """dhcpd\[\S+?:\s+({additional_info}[^~]+?)\s*$"""
  
}
```