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
    """\s({host}[^\s]+)\s+ftp-log end=({time}\d+)\s+[^,]*,"({event_name}[^"]+)","({user}[^"]+)","({src_host}[^"]+)","({src_ip}[a-fA-F\d.:]+)","({dest_ip}[a-fA-F\d.:]+)","({dest_port}\d+)?","({session_id}[^"]+)",""",
  ]


}
```