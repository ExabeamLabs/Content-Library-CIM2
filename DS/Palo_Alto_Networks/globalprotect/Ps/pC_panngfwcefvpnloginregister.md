#### Parser Content
```Java
{
Name = pan-ngfw-cef-vpn-login-register
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|""", """|GLOBALPROTECT|""", """=gateway-register""" ]

paloalto-globalprotect-template = {
    Vendor = Palo Alto Networks
    Product = GlobalProtect
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss"]
    Fields = [
      """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""
      """\s({host}[\w\-.]+?)\sCEF:""",
      """\sdvchost=({host}[\w\-.]+)""",
      """\|rt=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
      """PanOSLogTimeStamp=({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
      """PanOSSourceUserName =(({email_address}[^@=]+@[^\.=]+\.[^=]+)|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=""", """PanOSPrivateIPv(4|6)=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""", """PanOSPublicIPv(4|6)=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=""",
      """\sName =({operation}({event_name}[^=]+?))\s\w+=""",
      """PanOSEventID=({operation}({event_name}[^=]+?))\s\w+=""",
      """shost=({src_host}[\w\-.]+)\s\w+=""",
      """PanOSEndpointDeviceName =({src_host}[\w\-.]+)""",
      """outcome=({result}[^=]+?)\s\w+=""",
      """PanOSEventStatus=({result}[^=]+?)\s\w+=""",
      """PanOSAuthMethod=({auth_method}[^=]+?)\s\w+=""",
      """({app}GLOBALPROTECT)""",
      """PanOSEndpointOSVersion="({os}[^"]+?)"""",
      """PanOSSourceRegion=({src_country}[^=]+?)\s\w+=""",
      """PanOSDescription="*({additional_info}[^"=]+)"?\s\w+=""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    
}
```