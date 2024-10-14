#### Parser Content
```Java
{
Name = "fortinet-utm-kv-alert-trigger-success-ips1"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
Conditions = [
  """subtype="ips""""
  """action="""
  """service="""
]
Fields = [
  """date=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
  """\Wdevname="?({host}[^"]+?)"?(\s+\w+=|\s*$)"""
  """\Wprofile="({alert_type}[^"]+)""""
  """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wseverity="?({alert_severity}\w+)"""
  """\Wsrcport=({src_port}\d+)"""
  """\Wdstport=({dest_port}\d+)"""
  """\Whostname="(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|((www\.)?({dest_host}[\w\-\.]+)))""""
  """\Wservice="?({protocol}\w+)"""
  """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """\Wattack="({alert_name}[^"]+)""""
  """\Wmsg="({additional_info}[^"]+)""""
  """\Waction="({action}[^"]+)"""",
  """\Wtz="?({tz}[+-]\d+)"""
]
DupFields = [
  "alert_name->alert_subject"
]
ParserVersion = "v1.0.0"


}
```