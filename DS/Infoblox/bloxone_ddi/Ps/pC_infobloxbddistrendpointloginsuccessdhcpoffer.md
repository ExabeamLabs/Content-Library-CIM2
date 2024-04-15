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
""": ({event_name}DHCPOFFER) on ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) to ({dest_mac}[^\s]+)( \(({dest_host}[\w\-.]+)\))?\s+via ({dest_interface}[^\s]+)"""
  ]
  DupFields = [ "dest_host->user" ]


}
```