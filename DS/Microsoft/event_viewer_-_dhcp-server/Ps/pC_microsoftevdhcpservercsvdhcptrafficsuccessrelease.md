#### Parser Content
```Java
{
Name = microsoft-evdhcpserver-csv-dhcp-traffic-success-release
  Vendor = Microsoft
  Product = Event Viewer - DHCP-Server
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yy,HH:mm:ss"
  Conditions = [ """,Release,""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d,\d\d:\d\d:\d\d)""",
    """({event_name}Release),({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({src_host}[^,]+)?""",
  ]


}
```