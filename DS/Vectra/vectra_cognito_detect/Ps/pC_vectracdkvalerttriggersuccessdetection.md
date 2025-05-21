#### Parser Content
```Java
{
Name = vectra-cd-kv-alert-trigger-success-detection
 Vendor = Vectra
 Product = Vectra Cognito Detect
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """currentIP=""","""detection@""","""certainty="""]
 Fields = [
   """UTCTimeStart="+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
   """category="+({alert_type}[^"]+)"""",
   """type="+({alert_name}[^"]+)"""",
   """threat="+({alert_severity}[^"]+)"""",
   """hostname="+(?:IP-[\d.]+|({src_host}[^"]+))"""",
   """currentIP="+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
   """DestinationIP="+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
 ]


}
```