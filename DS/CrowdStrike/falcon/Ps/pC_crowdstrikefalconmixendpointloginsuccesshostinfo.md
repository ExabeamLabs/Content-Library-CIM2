#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-endpoint-login-success-hostinfo"
  ParserVersion = "v1.0.0"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  TimeFormat = "epoch"
  Conditions = [ 
""""event_simpleName":"HostInfo""""
""""aid"""" 
]
  Fields = [      
    """"timestamp":\s*"*({time}\d{13})"""",
    """"+MachineDn"+:"+CN\\*(=|u003d)?({dest_host}[^,]+)""",
    """"aid":"({aid}[^"]+)""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """suser=(system|({user}[\w\.\-]{1,40}\$?))""",
    """"MachineDomain":"({domain}[^"]+)"""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"SiteName":"({location}[^"]+)"""",
    """"cid":"({cid}[^"]+)"""
    """"event_platform":"({os}[^"]+)""""
  ]
  DupFields = [ "dest_host->host" ]


}
```