#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-endpoint-notification-discovererdevicetype
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """destinationServiceName =CrowdStrike""", """"discoverer_devicetype":"""", """"discoverer_aid":"""" ]
  Fields = [
    """"_time":"({time}\d{10})""",
    """"ComputerName":"({src_host}[^"]+)"""",
    """"(?i)mac":\s*"({src_mac}[^"]+)""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"cid":"({cid}[^"]+)""",
    """"discoverer_aid":"({aid}[^"]+)""",
    """suser=(system|({user}[\w\.\-]{1,40}\$?))""",
  ]


}
```