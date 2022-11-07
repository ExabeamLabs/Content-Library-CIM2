#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-network-session-success-listenip
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""event_simpleName":""""
"""NetworkListenIP""" 
]
  Fields = [
    """\"timestamp\":\"({time}\d{10})\"""",
    """\"LocalAddressIP4\":\"(0.0.0.0|0:0:0:0:0:0:0:0|({src_ip}[A-Fa-f:\d.]+))""",
    """\"LocalPort\":\"({src_port}\d+)""",
    """\"RemoteAddressIP4\":\"(0.0.0.0|0:0:0:0:0:0:0:0|({dest_ip}[A-Fa-f:\d.]+))""",
    """\"RemotePort\":\"({dest_port}\d+)""",
    """\"ConnectionDirection\":\"({direction}[^\"]+)""",
    """\"ContextProcessId\":\"({process_guid}[^\"]+)""",
    """\"event_simpleName\":\"({event_name}[^\"]+)""",
    """\"name\":\"({process_name}[^\"]+)""",
    """\"LocalAddressIP6\":\"(0.0.0.0|0:0:0:0:0:0:0:0|({src_ip}[A-Fa-f:\d.]+))""",
    """\"RemoteAddressIP6\":\"(0.0.0.0|0:0:0:0:0:0:0:0|({dest_ip}[A-Fa-f:\d.]+))""",
    """src-account-name\":\"({account_name}[^\"]+)""",
    """\"aid\":\"({aid}[^\"]+)"""
 ]


}
```