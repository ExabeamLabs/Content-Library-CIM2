#### Parser Content
```Java
{
Name = "entrust-ie-kv-endpoint-login-fail-authfail"
Vendor = "Entrust"
Product = "Entrust Identity Enterprise"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""] User """
""" failed authentication."""
""" Authentication Type: """
""" Application Name: """
""" Remote Address: """
]
Fields = [
"""\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])"""
""" User (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[^\s]+)) failed authentication"""
"""Authentication Type: ({auth_method}[^,]+),"""
"""Application Name: ({app}[^,]+),"""
"""Remote Address: ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```