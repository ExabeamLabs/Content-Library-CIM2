#### Parser Content
```Java
{
Name = pan-ngfw-cef-vpn-logout-success-logout
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|PAN-OS|""", """|GLOBALPROTECT|""", """PanOSEventID=gateway-logout""" ]

paloalto-globalprotect-template = {
    Vendor = Palo Alto Networks
    Product = GlobalProtect
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss"]
    Fields = [
      """\s({host}[\w\-.]+?)\sCEF:""",
      """PanOSLogTimeStamp=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
      """PanOSSourceUserName =(({email_address}[^@=]+@[^\.=]+\.[^=]+)|(({domain}[^\\=]+)\\+)?({user}[\w\.\-]{1,40}\$?))\s\w+=""", """PanOSPrivateIPv(4|6)=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""", """PanOSPublicIPv(4|6)=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """PanOSEventID=({event_name}[^=]+?)\s\w+=""",
      """PanOSEndpointDeviceName =({src_host}[\w\-.]+)""",
      """PanOSEventStatus=({result}[^=]+?)\s\w+=""",
      """PanOSAuthMethod=({auth_method}[^=]+?)\s\w+=""",
      """({app}GLOBALPROTECT)""",
      """PanOSEndpointOSVersion="({os}[^"]+?)"""",
      """PanOSSourceRegion=({src_country}[^=]+?)\s\w+=""",
      """PanOSDescription="({additional_info}[^"]+)"""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    
}
```