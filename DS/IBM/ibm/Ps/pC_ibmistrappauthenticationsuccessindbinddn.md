#### Parser Content
```Java
{
Name = "ibm-i-str-app-authentication-success-indbinddn"
Vendor = "IBM"
Product = "IBM"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""ind--bindDN"""
"""--Success"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+).*?ind--bindDN"""
"""uid=({user}[\w\.\-]{1,40}\$?)"""
"""client:\s*((:0|::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)(:({=src_port}\d+))?)\-*connectionID:"""
]
ParserVersion = "v1.0.0"


}
```