#### Parser Content
```Java
{
Name = microsoft-windows-csv-network-notification-success-dnsrenew
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  ParserVersion = v1.0.0
  Conditions = [ """,解放,""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s+\[""",
    """,(解放|期限切れ),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}[\w\-.]+)?,({dest_mac}[^,]+)?,"""
  ]
  DupFields = [ "dest_host->user" ]


}
```