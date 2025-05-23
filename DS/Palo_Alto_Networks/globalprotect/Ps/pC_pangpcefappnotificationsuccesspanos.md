#### Parser Content
```Java
{
Name = pan-gp-cef-app-notification-success-panos
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss", "MMM dd yyyy HH:mm:ss"]
  Conditions = [ """CEF:""", """|Palo Alto Networks|""", """|GLOBALPROTECT|""", """=gateway-config-release""" ]
  Fields = [
    """\sdvchost=({host}[^\s]+)"""
    """\sshost=({src_host}[\w\-.]+)\s""",
    """\srt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """suser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^\s@=]+))?""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+\w+=""",
    """PanOSHostID=({src_mac}[^=]+)\s+\w+=""",
    """\s(-|({host}[\w\-.]+?))\sCEF:""",
    """PanOSLogTimeStamp=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """PanOSSourceUserName =(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
    """PanOSPrivateIPv(4|6)=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """PanOSPublicIPv(4|6)=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """PanOSEventID=({event_name}[^=]+?)\s\w+=""",
    """PanOSEndpointDeviceName =({src_host}[\w\-.]+)""",
    """PanOSEventStatus=({result}[^=]+?)\s\w+=""",
    """PanOSAuthMethod=({auth_method}[^=]+?)\s\w+=""",
    """({app}GLOBALPROTECT)""",
    """PanOSEndpointOSVersion="({os}[^"]+?)"""",
    """PanOSSourceRegion=({src_country}[^=]+?)\s\w+=""",
    """PanOSDescription="({additional_info}[^"]+)"""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```