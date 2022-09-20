#### Parser Content
```Java
{
Name = pan-gp-cef-app-activity-success-portalgetconfig
 ParserVersion = "v1.0.0"
 Conditions = [ """PanOSEventIDValue=portal-getconfig""", """GLOBALPROTECT""", ]

paloalto-vpn-event = {
    Vendor = Palo Alto Networks
    Product = Palo Alto GlobalProtect
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    Fields = [
      """"receiveTimestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
      """PanOSSourceUserName =({user}[^=]+?)\s\w+=""",
      """PanOSPrivateIPv(4|6)=({dest_ip}[A-Fa-f\d:.]+)""",
      """PanOSPublicIPv(4|6)=({src_ip}[A-Fa-f\d:.]+)""",
      """PanOSDeviceName =({host}[\w\-.]+)""",
      """PanOSDescription=({additional_info}[^=]+)\s\w+=""",
      """PanOSEventStatus=({result}[^=]+?)\s\w+=""",
      """PanOSEventIDValue=({event_name}[^=]+?)\s\w+=""",
      """PanOSEndpointDeviceName =({src_host}[\w\-.]+)""",
      """PanOSEndpointOSVersion=({os}[^=]+?)\s\d""",
      """PanOSSourceRegion=({src_country}[^=]+?)\s\w+=""",
      """PanOSAuthMethod=({auth_method}[^=]+?)\s\w+=""",
      """({app}GLOBALPROTECT)"""
    
}
```