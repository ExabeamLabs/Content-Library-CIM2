#### Parser Content
```Java
{
Name = fortinet-utm-kv-alert-trigger-virus
  ParserVersion = "v1.0.0"
  Vendor = Fortinet
  Product = Fortinet UTM
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """subtype="virus"""", """action=""" ]
  Fields = [
    """\Wdate=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)""",
    """\Wdevname="*({host}[^\s"]+)"*(\s|")""",
    """\Wsrcip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdstip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Weventtype="({alert_name}[^"]+)"""",
    """\Wsubtype="({alert_type}[^"]+)"""",
    """\Wlogid="*({alert_id}\d+)(\s|")""",
    """\Wfilename="({malware_url}[^"]+)"""",
    """\Wfilename="({malware_file_name}[^"]+)"""",
    """\Wurl="({malware_url}[^"]+)"""",
    """\Wref="({additional_info}[^"]+)"""",
    """\Wuser="({user}[^"]+)"""",
    """\Wlevel="*({alert_severity}[^"\s]+)(\s|")""",
    """\Waction="({action}[^"]+)"""",
    """\Wsrcport=({src_port}\d+)""",
    """\Wdstport=({dest_port}\d+)""",
    """\Wservice="({protocol}[^"]+)"""",
  ]


}
```