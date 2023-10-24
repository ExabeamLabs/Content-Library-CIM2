#### Parser Content
```Java
{
Name = pan-gp-cef-app-notification-success-gatewayswitch
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Palo Alto Networks|PAN-OS|""", """|GLOBALPROTECT|""", """PanOSEventID=gateway-switch-to-ssl""" ]
  Fields = [
  """PanOSLogTimeStamp=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
  """\s*({host}[\w\-.]+)\s*CEF:""",
  """PanOSSourceUserName =(({domain}[^\\\s]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
  """PanOSEventID=({event_name}[^=]+?)\s\w+=""",
  """PanOSEndpointDeviceName =({src_host}[\w\-.]+)""",
  """PanOSEventStatus=({result}[^=]+?)\s\w+=""",
  """PanOSAuthMethod=({auth_method}[^=]+?)\s\w+=""",
  """({app}GLOBALPROTECT)""",
  """PanOSEndpointOSVersion="({os}[^"]+?)"""",
  """PanOSSourceRegion=({src_country}[^=]+?)\s\w+=""",
  """PanOSDescription="({additional_info}[^"]+)"""",
  """PanOSPrivateIPv(4|6)=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
  """PanOSPublicIPv(4|6)=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]
  ParserVersion = v1.0.0


}
```