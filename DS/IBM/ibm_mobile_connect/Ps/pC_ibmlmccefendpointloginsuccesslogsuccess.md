#### Parser Content
```Java
{
Name = "ibm-lmc-cef-endpoint-login-success-logsuccess"
Vendor = "IBM"
Product = "IBM Mobile Connect"
TimeFormat = "epoch"
Conditions = [
"""|IBM|HQ_LMC|"""
"""|LMC_Login_Success|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""dvc=({host}[a-fA-F:\d.]+)"""
"""dvchost=({host}[\w\-.]+)"""
"""shost=({src_host}[\w\-.]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dhost=({dest_host}[\w\-.]+)"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""deviceOutboundInterface=({src_network_type}.+?)\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```