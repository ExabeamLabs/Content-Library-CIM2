#### Parser Content
```Java
{
Name = infoblox-nios-str-network-notification-success-bindstate
  Vendor = Infoblox
  Product = Infoblox NIOS
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ dhcpd[""", """ FREE/BACKUP lease """, """ Bind-State """ ]
  Fields = [
    """\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+dhcpd\["""
    """dhcpd\[\S+?:\s+({additional_info}[^~]+?)\s*$"""
  ]


}
```