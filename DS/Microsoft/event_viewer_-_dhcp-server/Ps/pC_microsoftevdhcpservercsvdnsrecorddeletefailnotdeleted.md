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
    """,({event_name}DNS record not deleted),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({src_host}[^,]+)?""",
    """({failure_reason}DNS record not deleted)"""
  ]


}
```