#### Parser Content
```Java
{
Name = microsoft-mdhcplog-csv-dhcp-traffic-success-expired
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yy,HH:mm:ss"
  Conditions = [ """,Expired,""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d,\d\d:\d\d:\d\d)""",
    """({event_name}Expired),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,(({src_host}[\w\-.]+),)?""",
  ]


}
```