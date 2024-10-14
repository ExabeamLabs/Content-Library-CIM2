#### Parser Content
```Java
{
Name = "siteminder-symantecsm-cef-endpoint-authentication-success-associates"
Vendor = "SiteMinder"
Product = "Symantec SiteMinder"
TimeFormat = "epoch"
Conditions = [
"""|Computer Associates|"""
"""SiteMinder|"""
"""categoryOutcome=/Success"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""dvc=({host}[a-fA-F:\d.]+)"""
"""dvchost=({host}[\w\-.]+)"""
"""shost=({src_host}[\w\-.]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dhost=({dest_host}[\w\-.]+)"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""duser=(uid\\=)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```