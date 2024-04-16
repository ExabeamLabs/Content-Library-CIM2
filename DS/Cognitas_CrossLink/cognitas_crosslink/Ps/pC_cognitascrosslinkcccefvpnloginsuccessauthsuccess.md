#### Parser Content
```Java
{
Name = "cognitascrosslink-cc-cef-vpn-login-success-authsuccess"
Vendor = "Cognitas CrossLink"
Product = "Cognitas CrossLink"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Cognitas|CrossLink|"""
"""|Authentication Succeeded|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```