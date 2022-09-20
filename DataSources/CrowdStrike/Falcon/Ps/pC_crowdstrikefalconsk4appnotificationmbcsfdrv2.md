#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-notification-mbcsfdrv2
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = v1.0.0
  TimeFormat = "epoch_sec"
  Conditions = [ """sk4-audit-event""", """requestClientApplication=MB_CS_FDRv2""" ]
  Fields = [
    """requestClientApplication=({app}.+?)\s+""",
    """"aip":"({src_ip}[A-Fa-f:\d.]+)""",
    """"aid":"({aid}[^"]+)""",
    """"event_platform":"({os}[^"]+)""",
    """"Time":"({time}\d{10}).\d{10}""",
    """"Timezone":"({zone}[^"]+)"""",
    """"ComputerName":"({src_host}[^"]+)"""",
    """suser=(system|({user}[^\s]+))""",
    """"City":"({location_city}[^"]+)"""",
    """"Version":"({os_version}[^"]+)"""",
# cid is removed
    """"UserName":"({user}[^"]+)""",
    """AccountType":"({user_type}[^"]+)""",
    """UserSid_readable":"({user_sid}[^"]+)""",
    """LastLoggedOnHost":"({src_host}[^"]+)"""
    """LocalAddressIP4":"({src_ip}[^"]+)""",
    """MAC":"({src_mac}[^"]+)"""
  ]


}
```