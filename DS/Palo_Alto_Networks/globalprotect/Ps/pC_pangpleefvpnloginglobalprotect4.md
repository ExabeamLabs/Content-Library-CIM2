#### Parser Content
```Java
{
Name = pan-gp-leef-vpn-login-globalprotect-4
 Conditions = [ """LEEF:""", """|Palo Alto Networks|""", """|gateway-connected|""" ]
 ParserVersion = "v1.0.0"

leef-paloalto-vpn-event = {
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSS" , "MMM dd yyyy HH:mm:ss z" ]
  Fields = [
      """devTimeFormat=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)""",
      """devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
      """PublicIPv(4|6)=(\s|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
      """PrivateIPv(4|6)=(\s|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
      """AuthMethod=({auth_method}[^=]+?)\s\w+=""",
      """usrName =((({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^.]+)\.\w+)\s)|(({=domain}[^\\]+)\\+)?({=user}[\w\.\-]{1,40}))""",
      """DeviceName =({host}[\w\-.]+)""",
      """Description=({additional_info}[^=]+)\s\w+=""",
      """EventStatus=({result}[^=\|]+?)\|?\s*\w+=""",
      """Palo Alto Networks\|Prisma Access\|2.1\|({event_name}[^|]+)\|""",
      """EndpointDeviceName =({src_host}[\w\-.]+)""",
      """EndpointOSVersion="*({os}[^=]+?)\s\d""",
      """SourceRegion=({src_country}[^=]+?)\s\w+=""",
      """Portal=({app}GlobalProtect_External_Gateway)"""
    
}
```