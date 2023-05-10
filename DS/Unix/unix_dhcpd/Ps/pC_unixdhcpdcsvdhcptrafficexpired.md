#### Parser Content
```Java
{
Name = unix-dhcpd-csv-dhcp-traffic-expired
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """,Expired,""" ]
  Fields = [
    """\d\d:\d\d:\d\d,({event_name}[^,]+),({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})?,({src_host}[^,]+)?""",
  ]


}
```