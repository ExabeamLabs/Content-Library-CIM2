#### Parser Content
```Java
{
Name = "netmotionwireless-nw-str-endpoint-authentication-success-foruser"
Vendor = "NetMotion Wireless"
Product = "NetMotion Wireless"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""IMP: Indicating session"""
"""for user """
]
Fields = [
"""Indicating session 0x({session_id}[^\s]+)"""
"""Indicating session.+?for user ({domain}[^\\]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\("""
"""on device host\/({dest_host}[^.\s]+)"""
"""ing authentication mode ({auth_method}.+?) from POP"""
"""from POP address ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```