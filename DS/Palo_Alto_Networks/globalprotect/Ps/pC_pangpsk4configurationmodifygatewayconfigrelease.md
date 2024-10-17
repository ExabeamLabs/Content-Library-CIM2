#### Parser Content
```Java
{
Name = pan-gp-sk4-configuration-modify-gatewayconfigrelease
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
  ParserVersion = v1.0.0
  Conditions = [
    """PanOSEventIDValue=gateway-config-release""",
    """GLOBALPROTECT"""
  ]
  Fields = [
    """"receiveTimestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
    """PanOSSourceUserName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
    """PanOSPublicIPv(4|6)=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """PanOSPublicIPv(4|6)=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """PanOSDeviceName =({host}[\w\-.]+)""",
    """PanOSDescription=({additional_info}[^=]+)\s\w+=""",
    """PanOSEventStatus=({result}[^=]+?)\s\w+=""",
    """PanOSEventIDValue=({event_name}[^=]+?)\s\w+=""",
    """PanOSEndpointDeviceName =({src_host}[\w\-.]+)""",
    """PanOSEndpointOSVersion=({os}[^=]+?)\s\d""",
    """PanOSSourceRegion=({src_country}[^=]+?)\s\w+=""",
    """PanOSAuthMethod=({auth_method}[^=]+?)\s\w+=""",
    """({app}GLOBALPROTECT)"""
  ]


}
```