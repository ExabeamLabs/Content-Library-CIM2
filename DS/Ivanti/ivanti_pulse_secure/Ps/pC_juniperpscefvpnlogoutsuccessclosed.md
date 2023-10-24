#### Parser Content
```Java
{
Name = "juniper-ps-cef-vpn-logout-success-closed"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|"""
"""|Connection closed|"""
"""|Connection closed by user|"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"


}
```