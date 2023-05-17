#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-dns
  Product = Microsoft DHCP Log
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """,DNS の更新要求,""" ]
  ParserVersion = "v1.0.0"

microsoft-dns-renew-jp = {
  Vendor = Microsoft
  Fields = [
    """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d),""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s+\[""",
    """({time}\d+\/\d+\/\d+,\d+:\d+:\d+[\+\-]\d+:\d+)""",
    """<Identifier>({host}[^<]+)<\/Identifier>""",
    """,(DNS.*)?(更新|要求|成功|更新成功)([^,]+)?,({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}[^,]+),(|({dest_mac}[^,]+))?,"""
  ]
  DupFields = [ "dest_host->user" 
}
```