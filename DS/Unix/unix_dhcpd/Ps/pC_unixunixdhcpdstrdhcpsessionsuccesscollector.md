#### Parser Content
```Java
{
Name = "unix-unixdhcpd-str-dhcp-session-success-collector"
Vendor = "Unix"
Product = "Unix dhcpd"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ dhcpd: DHCPACK """
  """"message":""""
  """"collector":""""
]
Fields = [
  """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w.\-]+) dhcpd:"""
  """({event_name}DHCPACK)"""
  """DHCPACK to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? \((<no client hardware address>|({dest_mac}[a-fA-F\d.:]+))\) via ({dest_interface}[^\s\"]+)"""
  """DHCPACK on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? to ({dest_mac}[a-fA-F\d.:]+) (\(({dest_host}[\w\-.]+)\))?\s*via ({dest_interface}[^\s\"]+)"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```