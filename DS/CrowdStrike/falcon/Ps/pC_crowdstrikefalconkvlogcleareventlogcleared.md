#### Parser Content
```Java
{
Name = "crowdstrike-falcon-kv-log-clear-eventlogcleared"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"timestamp":"""", """"event_simpleName":"EventLogCleared"""" ]
  Fields = [
    """"timestamp":"({time}\d{10})""",
    """"event_simpleName":"({event_name}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# cid is removed
    """"event_platform":"({os}[^"]+)""",
    """"UserSid":"({user_sid}[^"]+)""",
    """"TargetFileName":"({target}[^"]+)""",
    """"UserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  ]


}
```