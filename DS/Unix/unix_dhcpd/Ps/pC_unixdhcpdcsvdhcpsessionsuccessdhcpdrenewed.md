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
    """({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),Renewed,(|({dest_host}[^,]+))"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [
    "dest_host->user"
  ]
  ParserVersion = "v1.0.0"


}
```