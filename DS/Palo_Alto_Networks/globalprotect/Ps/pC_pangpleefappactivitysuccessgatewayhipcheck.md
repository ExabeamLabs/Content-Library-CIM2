#### Parser Content
```Java
{
Name = pan-gp-leef-app-activity-success-gatewayhipcheck
 Conditions = [ """LEEF:""", """|Palo Alto Networks|""", """globalprotect""", """|gateway-hip-check|""" ]
 ParserVersion = "v1.0.0"

leef-paloalto-vpn-event = {
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
  Fields = [
      """devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
      """PublicIPv(4|6)=(\s|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
      """PrivateIPv(4|6)=(\s|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
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