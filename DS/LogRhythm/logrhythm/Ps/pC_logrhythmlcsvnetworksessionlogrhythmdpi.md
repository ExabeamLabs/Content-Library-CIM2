#### Parser Content
```Java
{
Name = logrhythm-l-csv-network-session-logrhythmdpi
  Vendor = LogRhythm
  Product = LogRhythm 
  ParserVersion = "v1.0.0"
  TimeFormat = "MM dd yyyy HH:mm:ss"
  Conditions = [ """LogRhythmDpi: EVT:""" ]
  Fields = [
    """({time}\d\d \d\d \d\d\d\d \d\d:\d\d:\d\d)\s+({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """LogRhythmDpi: EVT:\d{3}\s+\S+\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({src_port}\d+),({dest_port}\d+),({src_mac}[^\s,]+),({dest_mac}[^\s,]+)""",
  ]


}
```