#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-endpoint-name-modify-hostnamechanged
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Conditions = [ """"timestamp":"""", """"ComputerName":"""", """"event_simpleName":"HostnameChanged"""" ]
  Fields = [
    """"timestamp":"({time}\d+)""",
    """"ComputerName":"({host}[^"]+)""",
    """"event_simpleName":"({event_name}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"aip":"({src_ip}[A-Fa-f:\d.]+)""",
# cid is removed
    """"event_platform":"({os}[^"]+)""",
    """"id":"({user_sid}[^"]+)""",
  ]
  DupFields = ["event_name->event_code"]


}
```