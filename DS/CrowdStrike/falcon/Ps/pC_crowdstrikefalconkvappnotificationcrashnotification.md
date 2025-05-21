#### Parser Content
```Java
{
Name = "crowdstrike-falcon-kv-app-notification-crashnotification"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"timestamp":"""", """"event_simpleName":"CrashNotification"""" ]
  Fields = [
    """"timestamp":"({time}\d{10})""",
    """"event_simpleName":"({event_name}[^"]+)""",
    """"CrashDumpFilePath":"(|({file_path}({file_dir}[^"]*?)[\\\/]*({file_name}[^\\"]+?(\.({file_ext}[^\\\.\s"]+))?)))""",
    """"aid":"({aid}[^"]+)""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# cid is removed
    """"event_platform":"({os}[^"]+)""",
  ]


}
```