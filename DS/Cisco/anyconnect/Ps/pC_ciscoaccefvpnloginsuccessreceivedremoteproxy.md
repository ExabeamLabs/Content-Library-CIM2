#### Parser Content
```Java
{
Name = "cisco-ac-cef-vpn-login-success-receivedremoteproxy"
Vendor = "Cisco"
Product = "AnyConnect"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|CISCO|Cisco VPN|"""
"""|Received remote Proxy Host data in ID Payload|"""
"""sourceTranslatedAddress="""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\ssourceTranslatedAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sduser=(?:({domain}[^\s]+?)\\+)?({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
"""\ssrc=({src_translated_ip}[^\s]+)"""
"""\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdvc=({host}[^\s]+)"""
"""\sdvchost=({dest_host}[^\s]+)"""
"""\sdvchost=({host}[^\s]+)"""
"""\scs1=({realm}[^\s]+).*?cs1Label=Group"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```