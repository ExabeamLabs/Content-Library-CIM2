#### Parser Content
```Java
{
Name = "juniper-ps-cef-vpn-login-success-loginsucceeded"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|Pulse Secure Access|"""
"""|Login Succeeded|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdvchost=({dest_host}.+?)(\s+\w+=|$)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sshost=({src_host}.+?)(\s+\w+=|$)"""
"""\sdvchost=({host}.+?)(\s+\w+=|$)"""
"""\ssuser=({account}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```