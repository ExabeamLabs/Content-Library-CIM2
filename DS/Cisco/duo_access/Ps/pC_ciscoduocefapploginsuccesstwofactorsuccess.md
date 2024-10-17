#### Parser Content
```Java
{
Name = "cisco-duo-cef-app-login-success-twofactorsuccess"
Vendor = "Cisco"
Product = "Duo Access"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Duo Security|Two-factor|"""
"""outcome=SUCCESS"""
]
Fields = [
"""\s\d\d:\d\d:\d\d ({host}[^\s=]+)"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sintegration=({app}.+?)\s+\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```