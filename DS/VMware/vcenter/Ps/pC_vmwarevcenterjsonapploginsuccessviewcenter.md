#### Parser Content
```Java
{
Name = "vmware-vcenter-json-app-login-success-viewcenter"
Vendor = "VMware"
Product = "vCenter"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""" VIEWCENTER """
"""] ["""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""host\":\"({host}[^\"]+)"""
"""vim.event.({operation}[^\s\]]+)"""
"""\[User\s([\w\.]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?).+?\s"""
"""\[User.+?@({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({app}VM_VCenter)"""
]
ParserVersion = "v1.0.0"


}
```