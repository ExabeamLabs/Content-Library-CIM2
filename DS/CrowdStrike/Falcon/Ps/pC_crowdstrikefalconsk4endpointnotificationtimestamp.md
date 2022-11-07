#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-endpoint-notification-timestamp
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"timestamp":"""", """"event_simpleName":"LocalIpAddressIP4"""" ]
  Fields = [
    """"timestamp":"({time}\d{10})""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"aip":"({src_ip}[A-Fa-f:\d.]+)""",
# cid is removed
    """"event_platform":"({os}[^"]+)""",
    """"id":"({user_sid}[^"]+)""",
    """"LocalAddressIP4":"({dest_ip}[^"]+)""",
  ]


}
```