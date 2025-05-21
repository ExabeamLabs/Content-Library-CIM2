#### Parser Content
```Java
{
Name = "unix-dhcpd-str-dhcp-session-success-dhcprequest"
  Vendor = "Unix"
  Product = "Unix dhcpd"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """dhcpd"""
    """DHCPREQUEST for"""
  ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+dhcpd"""
    """DHCPREQUEST for ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """from ({dest_mac}[A-Fa-f:\d.]+)( \((?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({dest_host}[^)]+)\))? via ({dest_interface}[^\s\"]+)"""
    """({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,({dest_host}[^,]+)"""
  ]
  DupFields = [
    "dest_host->user"
  ]
  ParserVersion = "v1.0.0"


}
```