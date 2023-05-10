#### Parser Content
```Java
{
Name = microsoft-evdhcpserver-csv-dns-record-delete-fail-notdeleted
  Vendor = Microsoft
  Product = Event Viewer - DHCP-Server
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yy,HH:mm:ss"
  Conditions = [ """,DNS record not deleted,""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,({event_name}[^,]+),({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})?,({src_host}[^,]+)?""",
  ]


}
```