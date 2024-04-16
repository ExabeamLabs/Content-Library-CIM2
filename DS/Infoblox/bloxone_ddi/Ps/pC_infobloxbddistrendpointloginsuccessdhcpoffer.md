#### Parser Content
```Java
{
Name = "infoblox-bddi-str-endpoint-login-success-dhcpoffer"
  ParserVersion = "v1.0.0"
  Vendor = "Infoblox"
  Product = "BloxOne DDI"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" dhcpd[""",
""": DHCPOFFER """
  ]
  Fields = [
"""({host}\S+) dhcpd\[""",
"""\]: ({event_name}DHCPOFFER) on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? to ({dest_mac}[a-fA-F\d.:]+).+?via\s*({dest_interface}[^\s]+)"""
  ]


}
```