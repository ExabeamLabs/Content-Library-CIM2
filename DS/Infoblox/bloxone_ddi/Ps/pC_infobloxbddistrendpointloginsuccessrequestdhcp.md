#### Parser Content
```Java
{
Name = "infoblox-bddi-str-endpoint-login-success-requestdhcp"
  ParserVersion = "v1.0.0"
  Vendor = "Infoblox"
  Product = "BloxOne DDI"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" dhcpd[""",
""": received a REQUEST DHCP packet from """
  ]
  Fields = [
""" ({host}\S+) \S+ dhcpd\[""",
"""({event_name}REQUEST DHCP) packet from relay-agent ({dest_interface}\S+) with """,
""" for ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? \(({dest_mac}\S+)\)"""
  ]
  DupFields = [ "dest_host->user" ]


}
```