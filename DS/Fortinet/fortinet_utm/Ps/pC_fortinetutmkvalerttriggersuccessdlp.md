#### Parser Content
```Java
{
Name = "fortinet-utm-kv-alert-trigger-success-dlp"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
Conditions = [
  """subtype="dlp""""
  """action="""
]
Fields = [
  """date=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
  """\Wdevname="*({host}[^\s"]+)"*(\s|")"""
  """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wseverity="({alert_severity}[^"]+)""""
  """\Wsubtype="({alert_type}[^"]+)""""
  """\Wurl="({target}[^"]+)""""
  """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """\Wfiltertype="({alert_name}[^"]+)""""
  """\Waction="({action}[^"]+)""""
  """\Whostname="({src_host}[^"]+)""""
  """\Wsrcport=({src_port}\d+)"""
  """\Wdstport=({dest_port}\d+)"""
  """\Wservice="({protocol}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```