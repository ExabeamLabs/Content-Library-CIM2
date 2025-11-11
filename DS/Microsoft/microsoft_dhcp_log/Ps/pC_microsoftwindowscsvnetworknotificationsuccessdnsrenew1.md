#### Parser Content
```Java
{
Name = microsoft-windows-csv-network-notification-success-dnsrenew-1
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  ParserVersion = v1.0.0
  Conditions = [ """,期限切れ,""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s+\[""",
    """,(解放|期限切れ),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,({dest_mac}[^,]+)?,"""
  ]


}
```