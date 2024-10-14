#### Parser Content
```Java
{
Name = "rangeraudit-ra-kv-app-login-success-ranger"
Vendor = "RangerAudit"
Product = "RangerAudit"
TimeFormat = "epoch"
Conditions = [
"""ranger"""
"""Login Success:"""
"""requestId="""
]
Fields = [
"""\[({host}[^\]]+)"""
"""epoch=({time}\d{13})"""
"""requestId=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""loginId=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""({app}ranger)"""
]
ParserVersion = "v1.0.0"


}
```