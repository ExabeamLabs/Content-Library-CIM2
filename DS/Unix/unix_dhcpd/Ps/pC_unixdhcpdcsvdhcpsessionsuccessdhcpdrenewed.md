#### Parser Content
```Java
{
Name = "unix-dhcpd-csv-dhcp-session-success-dhcpdrenewed"
  Vendor = "Unix"
  Product = "Unix dhcpd"
  TimeFormat = "epoch"
  Conditions = [
    """dhcpd"""
    """,Renewed,"""
  ]
  Fields = [
    """\s({host}[^\s]+)\s+dhcpd"""
    """({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,(|({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```