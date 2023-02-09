#### Parser Content
```Java
{
Name = unix-dhcpd-csv-dns-record-delete-fail-notdeleted
  ParserVersion = v1.0.0
  Conditions = [ """,DNS record not deleted,""" ]

dhcpd-events-1= {
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d,({event_name}[^,]+),({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})?,({src_host}[^,]+)?""",
  
}
```