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
    """"timestamp":"({time}\d{13})""",
    """"ComputerName":"({host}[^"]+)""",
    """"event_simpleName":"({event_name}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# cid is removed
    """"event_platform":"({os}[^"]+)"""
  ]
  DupFields = ["event_name->event_code"]


}
```