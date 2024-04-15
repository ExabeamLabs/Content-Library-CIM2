#### Parser Content
```Java
{
Name = "juniper-ps-cef-vpn-logout-success-authenticated"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|"""
"""|Connection not authenticated yet|"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wsuser=(System|({user}[^\s]+))"""
"""\Wshost=({src_host}[\w\-.]+)"""
"""\Wmsg=({additional_info}.+?)\s+end="""
]
ParserVersion = "v1.0.0"


}
```