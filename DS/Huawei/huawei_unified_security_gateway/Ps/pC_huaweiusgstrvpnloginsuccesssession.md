#### Parser Content
```Java
{
Name = "huawei-usg-str-vpn-login-success-session"
Vendor = "Huawei"
Product = "Huawei Unified Security Gateway"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""SEC/"""
"""/SESSION"""
"""DevIP="""
""" VPN ID:"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)"""
"""Protocol:({protocol}[^;]+)"""
"""({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?;\s*({src_translated_ip}[^\s;]+?):({src_translated_port}\d+);\s*-->({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?;"""
"""\sname:(?!\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(({email_address}[^@;]+@[^@;]+)|({user}[^;]+));"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```