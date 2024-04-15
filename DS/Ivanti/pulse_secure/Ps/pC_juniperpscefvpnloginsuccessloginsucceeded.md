#### Parser Content
```Java
{
Name = "juniper-ps-cef-vpn-login-success-loginsucceeded"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|Pulse Secure Access|"""
"""|Login Succeeded|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdvchost=({dest_host}.+?)(\s+\w+=|$)"""
"""\ssuser=({user}.+?)(\s+\w+=|$)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sshost=({src_host}.+?)(\s+\w+=|$)"""
]
DupFields = [
"dest_ip->host"
"dest_host->host"
"user->account"
]
ParserVersion = "v1.0.0"


}
```