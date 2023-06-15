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
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
    """LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """MAC":"({src_mac}[^"]+)"""
  ]


}
```