#### Parser Content
```Java
{
Name = "infoblox-bddi-str-dhcp-session-success-dhcprequest"
  Vendor = "Infoblox"
  Product = "BloxOne DDI"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
    """dhcpd"""
    """DHCPREQUEST for"""
    """infoblox"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d([\+\-][^\s]+)?)\s+({host}[^\s]+)\s+dhcpd"""
    """({event_name}DHCPREQUEST) for ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """from ({dest_mac}[A-Fa-f:\d.]+)( \((?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})({dest_host}[^)]+)\))? via ({dest_interface}[^\s\"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```