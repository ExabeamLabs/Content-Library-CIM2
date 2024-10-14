#### Parser Content
```Java
{
Name = ftp-f-csv-ftp-close-success-sessionclosed
  ParserVersion = v1.0.0
  Vendor = FTP
  Product = FTP
  TimeFormat = "epoch_sec"
  Conditions = [ """ ftp-log end=""", """"Session Closed"""" ]
  Fields = [
    """\s({host}[^\s]+)\s+ftp-log end=({time}\d{10})\s+[^,]*,"({event_name}[^"]+)","({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_host}[^"]+)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","({=dest_port}\d+)?","({session_id}[^"]+)",""",
  ]


}
```