#### Parser Content
```Java
{
Name = "fortinet-utm-kv-alert-trigger-success-anomaly"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
Conditions = [
  """subtype="anomaly""""
  """action="""
]
Fields = [
  """date=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
  """\Wdevname="*({host}[^\s"]+)"*(\s|")"""
  """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wattack="({alert_subject}({alert_name}[^"]+))""""
  """\Wsubtype="({alert_type}[^"]+)""""
  """\Wattackid=({alert_id}\d+)(\s|")"""
  """\Wref="({malware_url}[^"]+)""""
  """\Wmsg="({additional_info}[^"]+)""""
  """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """\Wcrlevel="*({alert_severity}[^"\s]+)(\s|")"""
  """\Wsrcport=({src_port}\d+)"""
  """\Wdstport=({dest_port}\d+)"""
  """\Wservice="({protocol}[^\/\-"]+)"""
  """\Waction="({action}[^"]+)"""",
  """\Wtz="?({tz}[+-]\d+)"""
]
ParserVersion = "v1.0.0"


}
```