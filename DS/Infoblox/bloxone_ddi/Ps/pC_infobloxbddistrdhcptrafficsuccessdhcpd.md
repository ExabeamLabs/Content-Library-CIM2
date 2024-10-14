#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-traffic-success-dhcpd
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """]: DHCPINFORM from """ ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """({event_name}DHCPINFORM) from ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? via ({dest_interface}[^\s"]+)\sTransID\s({transaction_id}\w+)""",
    """from\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = ["transaction_id->trans_id"]
  ParserVersion = "v1.0.0"


}
```