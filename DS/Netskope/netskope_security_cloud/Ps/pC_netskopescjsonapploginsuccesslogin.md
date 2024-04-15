#### Parser Content
```Java
{
Name = "netskope-sc-json-app-login-success-login"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
Conditions = [
"""session_begin"""
"""activity": "Login Successful"""
]
Fields = [
""""dstip": "({host}[^"]+)""""
""""timestamp": ({time}\d{10})"""
""""user": "(?![^\s]+@[^\s]+)({user}[^"\s]+)""""
""""user": "(?=[^\s]+@[^\s]+)({email_address}[^"\s@]+@({email_domain}[^"\s@]+))""""
""""app": "({app}[^"]+)""""
""""dstip": "({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""srcip": "({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""browser": "(unknown|({browser}[^"]+))""""
""""os": "(unknown|({os}[^"]+))""""
""""access_method":\s*"({auth_method}[^"]+)"""",
""""object":\s*"(\s+"|(\s*(Unknown Unknown|unknown|Unknown|null|(?:<[^>=]+>[^"]+?)|({object}[^"]+?))\s*"))""",
]
ParserVersion = "v1.0.0"


}
```