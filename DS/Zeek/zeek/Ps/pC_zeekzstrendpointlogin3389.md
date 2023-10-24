#### Parser Content
```Java
{
Name = "zeek-z-str-endpoint-login-3389"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "epoch"
Conditions = [
""" 3389    """
""" Success RDP """
]
Fields = [
"""({time}\d{13})"""
"""([^\t]+\t){2}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\t]+))\t({src_port}\d+)"""
"""([^\t]+\t){4}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\t]+))\t({dest_port}\d+)"""
"""([^\t]+\t){11}({src_host}[^\t]+)"""
"""3389\t(?:\(empty\)|(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?))\tSuccess"""
]
ParserVersion = "v1.0.0"


}
```