#### Parser Content
```Java
{
Name = logrhythm-netmon-csv-rule-trigger-success-005
  Vendor = LogRhythm
  Product = NetMon 
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM  dd HH:mm:ss"
  Conditions = [ """ LogRhythmDpi""", """EVT:005 """ ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({host}[\w\-\.]+)\s+LogRhythmDpi"""
    """EVT:005\s+({rule}[^,]+),({session_id}[^,:]+)\S+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({src_port}\d+),({dest_port}\d+),({src_mac}[^,]+),({dest_mac}[^,]+),({protocol}\d+),\d+,\d+\/({bytes_in}\d+),\d+\/({bytes_out}\d+),\S+?,({packets_in}\d+)"""
  ]


}
```