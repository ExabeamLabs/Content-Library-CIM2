#### Parser Content
```Java
{
Name = microsoft-evdhcpserver-csv-app-notification-success-deleted
  Vendor = Microsoft
  Product = Event Viewer - DHCP-Server
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yy,HH:mm:ss"
  Conditions = [ """,Deleted,""" ]
  Fields = [
  """({event_code}\d+),({time}\d\d\/\d\d\/\d\d,\d\d:\d\d:\d\d)""",
	"""\d\d:\d\d:\d\d,({event_name}[^,]+),({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?,({src_host}[^,]+)?"""
  ]


}
```