#### Parser Content
```Java
{
Name = "huawei-usg-kv-vpn-login-success-logonsuccess"
Vendor = "Huawei"
Product = "Huawei Unified Security Gateway"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""UM/"""
"""/LOGONSUCCESS"""
"""Source IP="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)"""
""": User logon ({result}succeeded)"""
"""User Name =(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(?:unknown|({email_address}[^@,]+@[^@,]+)|({user}[^,]+)),"""
"""Source IP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```