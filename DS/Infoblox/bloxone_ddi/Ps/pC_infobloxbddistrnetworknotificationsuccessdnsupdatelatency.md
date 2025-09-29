#### Parser Content
```Java
{
Name = infoblox-bddi-str-network-notification-success-dnsupdatelatency
  ParserVersion = v1.0.0
  Conditions = [ """dhcpd[""", """dynamic DNS update latency:""" ]
  Fields = ${DLUnixParsersTemplates.s-infoblox-one-dhcp-dl-events.Fields}[
    """({event_name}dynamic DNS update latency)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]

s-infoblox-one-dhcp-dl-events = {
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+dhcpd\[""",
    """dhcpd\[\S+?:\s+({additional_info}[^~]+?)\s*$"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  
}
```