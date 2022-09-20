#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-network-traffic-success-connectip
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""event_simpleName":"NetworkConnectIP""" 
]
  Fields = [
    """hostname\":\"({host}[^\"]+)\"""",
    """\"timestamp\":\"({time}\d{10})\"""",
    """\"aid\":\"({aid}[^\"]+)""",
    """\"name\":\"({event_name}[^\"]+)\"""",
    """\"LocalAddressIP(4|6)\":\"(0:0:0:0:0:0:0:0|0.0.0.0|127.0.0.1|({src_ip}[^\"]+))""",
    """\"RemoteAddressIP(4|6)\":\"(0:0:0:0:0:0:0:0|0.0.0.0|127.0.0.1|({dest_ip}[^\"]+))""",
    """\"LocalPort\":\"({src_port}\d+)""",
    """\"RemotePort\":\"({dest_port}\d+)""",
    """\"ConnectionDirection\":\"({direction}(0|1))""",
    """\"Protocol\":\"({protocol}[^\"]+)""",
    """src-account-name\":\"({account_name}[^\"]+)""",
    """\"ContextProcessId\":\"({process_guid}[^\"]+)\""""
  ]


}
```