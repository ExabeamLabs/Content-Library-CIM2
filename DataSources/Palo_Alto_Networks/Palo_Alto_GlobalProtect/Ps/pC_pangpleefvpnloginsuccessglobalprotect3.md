#### Parser Content
```Java
{
Name = pan-gp-leef-vpn-login-success-globalprotect-3
 Conditions = [ """LEEF:""", """|Palo Alto Networks|""", """globalprotect""", """|gateway-register|""" ]
 ParserVersion = "v1.0.0"

leef-paloalto-vpn-event = {
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
  Fields = [
      """devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
      """PublicIPv(4|6)=(\s|({src_ip}[A-Fa-f\d:.]+))""",
      """PrivateIPv(4|6)=(\s|({dest_ip}[A-Fa-f\d:.]+))""",
      """AuthMethod=({auth_method}[^=]+?)\s\w+=""",
      """usrName =((({email_address}({user}[^@]+)@({domain}[^.]+)\.\w+)\s)|(({=domain}[^\\]+)\\+)?({=user}[^\s]+))""",
      """DeviceName =({src_host}[\w\-.]+)""",
      """Description=({additional_info}[^=]+)\s\w+=""",
      """EventStatus=({result}[^=]+?)\s\w+=""",
      """Palo Alto Networks\|Prisma Access\|2.1\|({event_name}[^|]+)\|""",
      """EndpointDeviceName =({host}[\w\-.]+)""",
      """EndpointOSVersion=({os}[^=]+?)\s\d""",
      """SourceRegion=({src_country}[^=]+?)\s\w+=""",
      """Portal=({app}GlobalProtect_External_Gateway)"""
    
}
```