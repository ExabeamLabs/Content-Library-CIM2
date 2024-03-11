#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-session-success-dynamicleases
  Vendor = Infoblox
  Product = BloxOne DDI
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """ BOOTREQUEST from """, """BOOTP from dynamic client and no dynamic leases""" ]
  Fields = [
    """\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s+({host}[\w.-]+)\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+dhcpd\[""",
    """\sdhcpd\[\d+\]:\s+BOOTREQUEST from ({dest_mac}\S+) via ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({dest_port}\d+))?:?\s"""
  ]


}
```